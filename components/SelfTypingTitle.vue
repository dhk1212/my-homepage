<template>
  <div class="title-text" />
</template>

<script>
export default {}
</script>

<style lang="scss">
// Love dynamically typed text? You're gonna love this
// Edit these strings to see them typed on the screen:
$strings: (
  'My name is Dahye Kim.' 'I am a student at HPI.' 'Scroll down to know more!'
);

// now for some timing (in seconds)
$durCharFwd: 0.1; // character typed
$durFullGap: 2; // time between typed/delete
$durCharBwd: 0.08; // character deleted
$durDoneGap: 1; // time between strings

// initializing some variables and functions ✊🏼
$charCount: 0;
$durTotal: 0;
@each $string in $strings {
  $charCount: $charCount + str-length($string);
  $durTotal: $durTotal +
    (str-length($string) * ($durCharFwd + $durCharBwd)) +
    $durFullGap +
    $durDoneGap;
}

@function percent($string, $letter, $modifier) {
  $stringsPast: $string - 1;
  $time: 0;
  @while $stringsPast > 0 {
    $time: $time +
      (
        ($durCharFwd + $durCharBwd) * (str-length(nth($strings, $stringsPast)))
      ) +
      $durFullGap +
      $durDoneGap;
    $stringsPast: $stringsPast - 1;
  }
  @if $letter <= str-length(nth($strings, $string)) {
    $time: $time + ($durCharFwd * ($letter - 1));
  } @else {
    $time: $time +
      ($durCharFwd * str-length(nth($strings, $string))) +
      $durFullGap +
      ($durCharBwd * ($letter - str-length(nth($strings, $string))));
  }
  @return ($time / $durTotal * 100 + $modifier) + '%';
}

$currentPercentage: 0;
// now THIS is where the magic happens... ✨
@keyframes typed {
  @for $i from 1 through length($strings) {
    // @for $j from 1 through (str-length(nth($strings, $i)) * 2 - 1) {
    @for $j from 1 through (str-length(nth($strings, $i)) * 2) {
      /* string #{$i}, char #{$j} */
      @if $j < str-length(nth($strings, $i)) * 2 {
        // not last character deleted
        #{percent($i, $j, 0)},
        #{percent($i, $j+1, -0.001)} {
          @if $j <= str-length(nth($strings, $i)) {
            content: quote(#{str_slice(nth($strings, $i), 1, $j)});
          } @else {
            content: quote(
              #{str_slice(
                  nth($strings, $i),
                  1,
                  str-length(nth($strings, $i)) -
                    ($j - str-length(nth($strings, $i)))
                )}
            );
          }
        }
      } @else {
        @if $i < length($strings) {
          // not last string
          #{percent($i, $j, 0)},
          #{percent($i+1, 1, -0.001)} {
            content: ' '; // zero-width space to retain element height
          }
        } @else {
          // last string
          #{percent($i, $j, 0)},
          100% {
            content: ' '; // zero-width space to retain element height
          }
        }
      }
    }
  }
}

@keyframes beam-blink {
  75% {
    border-color: transparent;
  }
}

.title-text {
  font-size: calc(10px + 2vw);
  font-family: 'VT323', monospace, sans-serif;
  color: #f08080; // hacker green
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  &::after {
    content: ' '; // zero-width space to retain element height
    position: relative;
    display: inline-block;
    padding-right: 3px;
    border-right: 10px solid rgba(#f08080, 0.75);
    border-right: calc(1.1vw + 4px) solid rgba(#f08080, 0.75);
    text-shadow: 0 0 5px rgba(240, 128, 128, 0.75);
    white-space: nowrap;
    animation: typed #{$durTotal + 's'} linear 1s infinite,
      beam-blink 1s infinite;
  }
}

// body[onload] {
// 	&::before, &::after { display: none !important; }
// 	background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/1580009/codepen_css-typed-this.png) center / cover;
// }
</style>
