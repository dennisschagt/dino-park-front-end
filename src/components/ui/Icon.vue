<template>
  <svg
    viewBox="0 0 24 24"
    aria-hidden="true"
    role="presentation"
    focusable="false"
    :width="width"
    :height="height"
  >
    <template v-if="id === 'user'">
      <path
        fill="currentColor"
        d="M20.2 18.3v1.8c0 .54-.36.9-.9.9s-.9-.36-.9-.9v-1.8c0-1.53-1.17-2.7-2.7-2.7H8.5c-1.53 0-2.7 1.17-2.7 2.7v1.8c0 .54-.36.9-.9.9s-.9-.36-.9-.9v-1.8c0-2.52 1.98-4.5 4.5-4.5h7.2c2.52 0 4.5 1.98 4.5 4.5zM7.6 7.5C7.6 4.98 9.58 3 12.1 3s4.5 1.98 4.5 4.5-1.98 4.5-4.5 4.5-4.5-1.98-4.5-4.5zm1.8 0c0 1.53 1.17 2.7 2.7 2.7 1.53 0 2.7-1.17 2.7-2.7 0-1.53-1.17-2.7-2.7-2.7-1.53 0-2.7 1.17-2.7 2.7z"
      />
    </template>
    <template v-else-if="id === 'dashboard'">
      <path
        fill="currentColor"
        d="M13 12.228c1.725.45 3 2.035 3 3.922 0 2.237-1.79 4.05-4 4.05s-4-1.813-4-4.05a4.043 4.043 0 0 1 3-3.922V9.063c0-.56.448-1.013 1-1.013s1 .453 1 1.012v3.166zM12 4c4.97 0 9 4.08 9 9.113 0 .559-.448 1.012-1 1.012s-1-.453-1-1.012c0-3.915-3.134-7.088-7-7.088s-7 3.173-7 7.088c0 .559-.448 1.012-1 1.012s-1-.453-1-1.012C3 8.08 7.03 4 12 4zm0 10.125c-1.105 0-2 .907-2 2.025 0 1.118.895 2.025 2 2.025s2-.907 2-2.025c0-1.118-.895-2.025-2-2.025z"
      />
    </template>
    <template v-else-if="id === 'bell'">
      <path
        fill="currentColor"
        d="M14.127 19.773A2.466 2.466 0 0 1 12 21c-.41 0-.818-.082-1.227-.327a2.377 2.377 0 0 1-.9-.9c-.246-.41-.082-.9.327-1.146.41-.245.9-.082 1.145.328.082.081.164.245.328.327.409.245.9.082 1.145-.327.246-.41.737-.491 1.146-.328.409.164.409.737.163 1.146zM21 16.09c0 .49-.327.818-.818.818H3.818c-.49 0-.818-.327-.818-.818 0-.491.327-.818.818-.818.9 0 1.637-.737 1.637-1.637v-4.09C5.455 5.945 8.4 3 12 3s6.545 2.945 6.545 6.545v4.091c0 .9.737 1.637 1.637 1.637.49 0 .818.327.818.818zm-3.682-.818a3.724 3.724 0 0 1-.409-1.637v-4.09c0-2.7-2.209-4.91-4.909-4.91-2.7 0-4.91 2.21-4.91 4.91v4.09c0 .573-.163 1.146-.408 1.637h10.636z"
      />
    </template>
    <template v-else-if="id === 'sliders'">
      <path
        fill="currentColor"
        d="M5.25 11V5.75c0-.45.3-.75.75-.75s.75.3.75.75V11c0 .45-.3.75-.75.75s-.75-.3-.75-.75zm6.75.75c-.45 0-.75.3-.75.75v6.75c0 .45.3.75.75.75s.75-.3.75-.75V12.5c0-.45-.3-.75-.75-.75zm6 1.5c.45 0 .75-.3.75-.75V5.75c0-.45-.3-.75-.75-.75s-.75.3-.75.75v6.75c0 .45.3.75.75.75zm-9.75 0h-4.5c-.45 0-.75.3-.75.75s.3.75.75.75h1.5v4.5c0 .45.3.75.75.75s.75-.3.75-.75v-4.5h1.5c.45 0 .75-.3.75-.75s-.3-.75-.75-.75zm6-4.5h-1.5v-3c0-.45-.3-.75-.75-.75s-.75.3-.75.75v3h-1.5c-.45 0-.75.3-.75.75s.3.75.75.75h4.5c.45 0 .75-.3.75-.75s-.3-.75-.75-.75zm6 6h-4.5c-.45 0-.75.3-.75.75s.3.75.75.75h1.5v3c0 .45.3.75.75.75s.75-.3.75-.75v-3h1.5c.45 0 .75-.3.75-.75s-.3-.75-.75-.75z"
      />
    </template>
    <template v-else-if="id === 'toggle-right'">
      <path
        fill="currentColor"
        d="M15 6H9c-3.3 0-6 2.7-6 6s2.7 6 6 6h6c3.3 0 6-2.7 6-6s-2.7-6-6-6zm0 10.5H9A4.513 4.513 0 0 1 4.5 12c0-2.475 2.025-4.5 4.5-4.5h6c2.475 0 4.5 2.025 4.5 4.5s-2.025 4.5-4.5 4.5zM15 9c-1.65 0-3 1.35-3 3s1.35 3 3 3 3-1.35 3-3-1.35-3-3-3zm0 4.5c-.825 0-1.5-.675-1.5-1.5s.675-1.5 1.5-1.5 1.5.675 1.5 1.5-.675 1.5-1.5 1.5z"
      />
    </template>
    <template v-else-if="id === 'log-out'">
      <path
        fill="currentColor"
        d="M11.373 20.182c0 .49-.328.818-.82.818H6.459C5.065 21 4 19.936 4 18.545V5.455C4 4.064 5.065 3 6.458 3h4.096c.491 0 .819.327.819.818 0 .491-.328.818-.82.818H6.459c-.492 0-.82.328-.82.819v13.09c0 .491.328.819.82.819h4.096c.491 0 .819.327.819.818zm8.93-7.855c.081-.163.081-.409 0-.654-.083-.082-.083-.164-.165-.246l-3.276-3.272a.793.793 0 0 0-1.147 0 .79.79 0 0 0 0 1.145l1.884 1.882H9.734c-.491 0-.819.327-.819.818 0 .49.328.818.82.818h7.864L15.715 14.7a.79.79 0 0 0 0 1.145c.163.164.41.246.573.246.164 0 .41-.082.574-.246l3.276-3.272c.082-.082.164-.164.164-.246z"
      />
    </template>
    <template v-else-if="id === 'chevron-up'">
      <polyline
        points="18 15 12 9 6 15"
        stroke="currentColor"
        stroke-width="2"
        stroke-line-ap="round"
        fill="none"
        stroke-linejoin="round"
      />
    </template>
    <template v-else-if="id === 'chevron-down'">
      <polyline
        points="6 9 12 15 18 9"
        stroke="currentColor"
        stroke-width="2"
        stroke-line-ap="round"
        fill="none"
        stroke-linejoin="round"
      />
    </template>
    <template v-else-if="id === 'chevron-right'">
      <polyline
        points="9 18 15 12 9 6"
        stroke="currentColor"
        stroke-width="2"
        stroke-line-ap="round"
        fill="none"
        stroke-linejoin="round"
      />
    </template>
    <template v-else-if="id === 'chevron-left'">
      <polyline
        points="15 18 9 12 15 6"
        stroke="currentColor"
        stroke-width="2"
        stroke-line-ap="round"
        fill="none"
        stroke-linejoin="round"
      />
    </template>
    <template v-else-if="id === 'org-chart'">
      <path
        d="M11.5 12a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zm0 2a3.5 3.5 0 1 1 0-7 3.5 3.5 0 0 1 0 7zm7 8a3.5 3.5 0 1 1 0-7 3.5 3.5 0 0 1 0 7zm0-2a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zM3.5 7a3.5 3.5 0 1 1 0-7 3.5 3.5 0 0 1 0 7zm0-2a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zM3 7h1v1H3V7zm0 2h1v1H3V9zm1 3h-.5a.5.5 0 0 1-.5-.5V11h1v1zm1 0v-1h1v1H5zm2 0v-1h1v1H7zm4 2h1v1h-1v-1zm0 2h1v1h-1v-1zm1 3h-.5a.5.5 0 0 1-.5-.5V18h1v1zm1 0v-1h1v1h-1z"
        fill="currentColor"
        fill-rule="nonzero"
      />
    </template>
    <template v-else-if="id === 'at-sign'">
      <circle
        cx="12"
        cy="12"
        r="4"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
      <path
        d="M16 8v5a3 3 0 0 0 6 0v-1a10 10 0 1 0-3.92 7.94"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </template>
    <template v-else-if="id === 'crown'">
      <path
        id="a"
        d="M20.085 19.099a1.05 1.05 0 0 1 1.046 1.05c0 .572-.508 1.051-1.087 1.051H1.846A1.053 1.053 0 0 1 .8 20.15c0-.577.472-1.051 1.046-1.051h18.239zM19.46 1.133c.72-.617 1.74-.269 1.74.735v14.196c0 .568-.46 1.03-1.026 1.03H1.891a1.029 1.029 0 0 1-1.026-1.03V1.827c0-.98 1.058-1.328 1.75-.73l3.76 3.362 3.823-3.369c.425-.388.976-.384 1.435-.002l3.936 3.482 3.89-3.437zm-.312 3.172l-2.852 2.436c-.4.401-1.051.401-1.442.008l-3.936-3.482-3.824 3.371c-.34.323-.995.366-1.44.003L2.917 4.287v10.746h16.231V4.305z"
        fill="currentColor"
      />
    </template>
    <template v-else-if="id === 'book'">
      <path
        d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
      <path
        d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </template>
    <template v-else-if="id === 'bookmark'">
      <path
        d="M19 21l-7-5-7 5V5a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2z"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </template>
    <template v-else-if="id === 'mail'">
      <path
        d="m9 17.333a8.333 8.333 0 1 0 0-16.666 8.333 8.333 0 0 0 0 16.666zm4.605-9.505a2.883 2.883 0 0 1 -.49.426 93.757 93.757 0 0 0 -2.437 1.689c-.411.303-.92.675-1.454.675h-.01c-.533 0-1.042-.372-1.453-.675-.798-.583-1.62-1.136-2.433-1.69a2.737 2.737 0 0 1 -.495-.425v3.887c0 .43.353.783.784.783h7.205c.43 0 .783-.352.783-.783zm0-1.743a.789.789 0 0 0 -.783-.783h-7.205c-.524 0-.784.41-.784.89 0 .446.495 1 .842 1.234.759.529 1.528 1.057 2.286 1.59.318.221.857.672 1.253.672h.01c.397 0 .935-.45 1.253-.671.76-.534 1.528-1.062 2.291-1.59.431-.3.837-.794.837-1.342z"
        fill="currentColor"
        fill-rule="evenodd"
      />
    </template>
    <template v-else-if="id === 'check'">
      <polyline
        points="20 6 9 17 4 12"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
      />
    </template>
    <template v-else-if="id === 'github'">
      <path
        d="M17.08 17.318a6.13 6.13 0 0 1 .306 1.895v3.79c0 .598-.408.997-1.02.997-.613 0-1.022-.399-1.022-.997v-3.89c.102-.797-.204-1.396-.714-1.894-.306-.3-.409-.698-.204-.997.102-.4.51-.599.816-.699 2.96-.299 5.716-1.296 5.716-5.983 0-1.097-.408-2.194-1.224-3.091-.307-.3-.307-.699-.205-.998.307-.797.307-1.595.102-2.393-.51.1-1.326.399-2.653 1.296-.205.2-.51.2-.817.1a12.487 12.487 0 0 0-6.635 0c-.306.1-.612.1-.919-.1-1.225-.897-2.143-1.196-2.654-1.296-.204.798-.204 1.596.102 2.393.102.4.102.798-.204.998-.816.897-1.225 1.994-1.225 3.091 0 4.687 2.756 5.684 5.717 5.983.408 0 .714.3.816.699.102.398 0 .797-.204.997-.51.498-.714 1.097-.714 1.795v3.889c0 .598-.409.997-1.021.997-.613 0-1.021-.399-1.021-.997v-1.695c-3.062.498-4.39-1.197-5.308-2.294-.408-.499-.714-.897-1.123-.997-.51-.1-.918-.698-.714-1.197.102-.498.714-.897 1.225-.698 1.02.3 1.633.997 2.245 1.695.817 1.097 1.531 1.895 3.675 1.496v-.1c0-.598.102-1.296.306-1.795-2.858-.598-5.92-2.393-5.92-7.678 0-1.496.51-2.892 1.429-3.99-.408-1.395-.306-2.692.306-3.988a.91.91 0 0 1 .613-.599c.408-.1 1.735-.299 4.49 1.397 2.247-.499 4.594-.499 6.738 0C18.815.764 20.244.964 20.652 1.063c.306.1.51.3.613.599.51 1.296.612 2.593.306 3.889A6.175 6.175 0 0 1 23 9.54c0 5.684-3.47 7.28-5.92 7.778z"
        fill="currentColor"
        fill-rule="evenodd"
      />
    </template>
    <template v-else-if="id === 'discourse'">
      <path
        d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"
        fill="none"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke="currentColor"
      />
    </template>
    <template v-else-if="id === 'lock'">
      <path
        d="M19 10h-1V7c0-3.3-2.7-6-6-6S6 3.7 6 7v3H5c-1.7 0-3 1.3-3 3v7c0 1.7 1.3 3 3 3h14c1.7 0 3-1.3 3-3v-7c0-1.7-1.3-3-3-3zM8 7c0-2.2 1.8-4 4-4s4 1.8 4 4v3H8V7zm12 13c0 .6-.4 1-1 1H5c-.6 0-1-.4-1-1v-7c0-.6.4-1 1-1h14c.6 0 1 .4 1 1v7z"
        fill="currentColor"
      />
    </template>
    <template v-else-if="id === 'phone-forwarded'">
      <path
        fill="currentColor"
        fill-rule="evenodd"
        d="M23.711 5.974l-4.196 4.192c-.21.21-.42.314-.735.314-.314 0-.524-.104-.734-.314a1.012 1.012 0 0 1 0-1.467l2.413-2.41h-5.875c-.63 0-1.05-.42-1.05-1.049s.42-1.048 1.05-1.048h5.875l-2.413-2.41a1.012 1.012 0 0 1 0-1.468c.42-.419 1.05-.419 1.469 0l4.196 4.193c.105.104.21.21.21.314.105.21.105.524 0 .838 0 .105-.105.21-.21.315zm-.734 11.738v3.144c0 .838-.315 1.677-.944 2.2-.63.525-1.364.944-2.203.944h-.315c-3.358-.42-6.715-1.572-9.548-3.354a22.05 22.05 0 0 1-6.61-6.602C1.47 11.214.315 7.86 0 4.507 0 3.668.21 2.83.734 2.2a3.242 3.242 0 0 1 2.099-1.153H6.295c1.574 0 2.938 1.153 3.148 2.725.105.943.314 1.886.63 2.725.419 1.153.104 2.41-.735 3.354l-.735.733c1.26 1.887 2.833 3.563 4.827 4.821l.734-.734c.84-.838 2.203-1.152 3.357-.733.84.314 1.784.524 2.728.629 1.574.21 2.728 1.572 2.728 3.144zm-2.098 0c0-.524-.42-.943-.945-1.048-1.049-.105-2.098-.42-3.147-.839-.42-.104-.84-.104-1.154.21l-1.364 1.362c-.315.315-.84.42-1.26.21A17.206 17.206 0 0 1 6.296 10.9c-.105-.42 0-.944.315-1.258l1.364-1.363c.21-.21.315-.733.21-1.048-.42-1.048-.63-2.096-.84-3.144 0-.524-.524-.943-1.049-.943H3.148c-.315 0-.63.21-.84.42-.105.209-.21.419-.21.733.315 3.04 1.364 5.974 3.043 8.594 1.574 2.41 3.567 4.506 5.98 5.974 2.623 1.676 5.561 2.725 8.604 3.039.42 0 .63-.105.839-.314.21-.21.315-.42.315-.734v-3.144z"
      />
    </template>
    <template v-else-if="id === 'private'">
      <path
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M17.94 17.94A10.07 10.07 0 0 1 12 20c-7 0-11-8-11-8a18.45 18.45 0 0 1 5.06-5.94M9.9 4.24A9.12 9.12 0 0 1 12 4c7 0 11 8 11 8a18.5 18.5 0 0 1-2.16 3.19m-6.72-1.07a3 3 0 1 1-4.24-4.24"
      />
      <line
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        x1="1"
        y1="1"
        x2="23"
        y2="23"
      />
    </template>
    <template v-else-if="id === 'triangle'">
      <path
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"
      />
    </template>
    <template v-else-if="id === 'activity'">
      <polyline
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        points="22 12 18 12 15 21 9 3 6 12 2 12"
      />
    </template>
    <template v-else-if="id === 'world'">
      <g
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <circle cx="12" cy="12" r="10" />
        <line x1="2" y1="12" x2="22" y2="12" />
        <path
          d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"
        />
      </g>
    </template>
    <template v-else-if="id === 'staff'">
      <path
        fill="currentColor"
        d="M19 2H5C3.3 2 2 3.3 2 5v14c0 1.7 1.3 3 3 3h14c1.7 0 3-1.3 3-3V5c0-1.7-1.3-3-3-3zm1 17c0 .6-.4 1-1 1H5c-.6 0-1-.4-1-1V5c0-.6.4-1 1-1h14c.6 0 1 .4 1 1v14zm-4.536-4.908c0-.483-.085-.903-.256-1.26a2.693 2.693 0 0 0-.806-.959c-.366-.283-.942-.588-1.728-.915-.698-.289-1.182-.52-1.45-.696-.269-.176-.462-.363-.579-.56a1.377 1.377 0 0 1-.176-.715c0-.405.147-.73.44-.977.293-.247.722-.37 1.289-.37.747 0 1.596.2 2.549.6l.556-1.428c-1.015-.45-2.036-.674-3.061-.674-1.07 0-1.922.257-2.556.77-.635.512-.953 1.215-.953 2.109 0 .712.2 1.323.601 1.83.4.508 1.089.96 2.065 1.356.948.38 1.573.71 1.875.988.303.279.455.618.455 1.018 0 .445-.165.799-.495 1.062-.33.264-.84.396-1.534.396a6.6 6.6 0 0 1-1.535-.198 8.082 8.082 0 0 1-1.556-.542v1.656c.771.375 1.763.563 2.974.563 1.21 0 2.16-.27 2.849-.813.688-.541 1.032-1.289 1.032-2.24z"
      />
    </template>
    <template v-else-if="id === 'x'">
      <line
        x1="18"
        y1="6"
        x2="6"
        y2="18"
        stroke="currentColor"
        stroke-width="2"
      />
      <line
        x1="6"
        y1="6"
        x2="18"
        y2="18"
        stroke="currentColor"
        stroke-width="2"
      />
    </template>
    <template v-else-if="id === 'plus'">
      <path
        fill="currentColor"
        d="M20 12c0 .6-.4 1-1 1h-6v6c0 .6-.4 1-1 1s-1-.4-1-1v-6H5c-.6 0-1-.4-1-1s.4-1 1-1h6V5c0-.6.4-1 1-1s1 .4 1 1v6h6c.6 0 1 .4 1 1z"
      />
    </template>
    <template v-else-if="id === 'envelope'">
      <path
        fill="currentColor"
        d="M20 3H4C2.3 3 1 4.3 1 6v12c0 1.7 1.3 3 3 3h16c1.7 0 3-1.3 3-3V6c0-1.7-1.3-3-3-3zM4 5h16c.4 0 .7.2.9.6L12 11.8 3.1 5.6c.2-.4.5-.6.9-.6zm16 14H4c-.6 0-1-.4-1-1V7.9l8.4 5.9c.2.1.4.2.6.2.2 0 .4-.1.6-.2L21 7.9V18c0 .6-.4 1-1 1z"
      />
    </template>
    <template v-else-if="id === 'keys'">
      <path
        d="M2,20.0001 L2,5.00004167 L22.0000778,5.00004167 L22.0000778,20.0001 L2,20.0001 Z M3.66708982,18.3338435 L20.3338213,18.3338435 L20.3338213,6.66671481 L3.66708982,6.66671481 L3.66708982,18.3338435 Z M12.8333755,10.0000611 L12.8333755,8.33338796 L14.9167169,8.33338796 L14.9167169,10.0000611 L12.8333755,10.0000611 Z M9.08336088,10.0000611 L9.08336088,8.33338796 L11.5833706,8.33338796 L11.5833706,10.0000611 L9.08336088,10.0000611 Z M5.3333463,10.0000611 L5.3333463,8.33338796 L7.83335602,8.33338796 L7.83335602,10.0000611 L5.3333463,10.0000611 Z M16.58339,13.3334074 L16.58339,11.6667343 L18.6667315,11.6667343 L18.6667315,13.3334074 L16.58339,13.3334074 Z M13.2500437,13.3334074 L13.2500437,11.6667343 L15.3333852,11.6667343 L15.3333852,13.3334074 L13.2500437,13.3334074 Z M9.91669745,13.3334074 L9.91669745,11.6667343 L12.0000389,11.6667343 L12.0000389,13.3334074 L9.91669745,13.3334074 Z M5.3333463,13.3334074 L5.3333463,11.6667343 L8.66669259,11.6667343 L8.66669259,13.3334074 L5.3333463,13.3334074 Z M16.1667218,10.0000611 L16.1667218,8.33338796 L18.6667315,8.33338796 L18.6667315,10.0000611 L16.1667218,10.0000611 Z M5.3333463,16.6667537 L5.3333463,15.0000806 L18.6667315,15.0000806 L18.6667315,16.6667537 L5.3333463,16.6667537 Z"
        fill="currentColor"
      />
    </template>
    <template v-else-if="id === 'chain'">
      <path
        fill="currentColor"
        d="M10 17c0 .6-.4 1-1 1H6c-3.3 0-6-2.7-6-6s2.7-6 6-6h3c.6 0 1 .4 1 1s-.4 1-1 1H6c-2.2 0-4 1.8-4 4s1.8 4 4 4h3c.6 0 1 .4 1 1zm8-11h-3c-.6 0-1 .4-1 1s.4 1 1 1h3c2.2 0 4 1.8 4 4s-1.8 4-4 4h-3c-.6 0-1 .4-1 1s.4 1 1 1h3c3.3 0 6-2.7 6-6s-2.7-6-6-6zM7 12c0 .6.4 1 1 1h8c.6 0 1-.4 1-1s-.4-1-1-1H8c-.6 0-1 .4-1 1z"
      />
    </template>
    <template v-else-if="id === 'pencil'">
      <path
        fill="currentColor"
        d="M21.7 7.3l-5-5c-.4-.4-1-.4-1.4 0l-13 13c-.2.2-.3.4-.3.7v5c0 .6.4 1 1 1h5c.3 0 .5-.1.7-.3l13-13c.4-.4.4-1 0-1.4zM7.6 20H4v-3.6l12-12L19.6 8l-12 12z"
      />
    </template>
    <template v-else-if="id === 'irc'">
      <path
        fill="currentColor"
        d="M19 2H5C3.3 2 2 3.3 2 5v16c0 .4.2.8.6.9.1.1.3.1.4.1.3 0 .5-.1.7-.3L7.4 18H19c1.7 0 3-1.3 3-3V5c0-1.7-1.3-3-3-3zm1 13c0 .6-.4 1-1 1H7c-.3 0-.5.1-.7.3L4 18.6V5c0-.6.4-1 1-1h14c.6 0 1 .4 1 1v10z"
      />
    </template>
    <template v-else-if="id === 'email'">
      <path
        fill="currentColor"
        d="M20 3H4C2.3 3 1 4.3 1 6v12c0 1.7 1.3 3 3 3h16c1.7 0 3-1.3 3-3V6c0-1.7-1.3-3-3-3zM4 5h16c.4 0 .7.2.9.6L12 11.8 3.1 5.6c.2-.4.5-.6.9-.6zm16 14H4c-.6 0-1-.4-1-1V7.9l8.4 5.9c.2.1.4.2.6.2.2 0 .4-.1.6-.2L21 7.9V18c0 .6-.4 1-1 1z"
      />
    </template>
    <template v-else-if="id === 'phone'">
      <path
        fill="currentColor"
        d="M20.388 13.959c-.904-.1-1.808-.301-2.612-.603-1.105-.402-2.31-.1-3.214.703l-.704.704c-1.808-1.206-3.415-2.713-4.62-4.621l.703-.704c.803-.803 1.105-2.11.703-3.214a11.007 11.007 0 0 1-.603-2.612C9.841 2.105 8.534 1 7.027 1H3.712c-.803.1-1.507.502-2.009 1.105S1 3.511 1 4.315c.301 3.215 1.507 6.43 3.215 9.142a21.124 21.124 0 0 0 6.328 6.328C13.256 21.594 16.47 22.7 19.685 23h.301c.804 0 1.608-.301 2.11-.904.502-.603.904-1.306.904-2.11v-3.013c0-1.507-1.105-2.813-2.612-3.014zm.603 3.014v3.013c0 .302-.1.503-.302.703-.2.201-.401.302-.803.302-2.913-.302-5.726-1.306-8.238-2.913-2.31-1.407-4.219-3.416-5.726-5.726C4.315 9.84 3.311 7.027 3.01 4.114c0-.301.1-.502.201-.703.201-.201.502-.402.804-.402h3.013c.503 0 .905.402 1.005.904.1 1.005.402 2.11.804 3.014.1.402 0 .804-.201 1.105L7.329 9.237a1.068 1.068 0 0 0-.201 1.206 16.484 16.484 0 0 0 6.43 6.43c.4.2.903.2 1.205-.202l1.305-1.306c.302-.301.704-.402 1.106-.2 1.004.401 2.009.602 3.013.803.402.1.804.502.804 1.005z"
      />
    </template>
    <template v-else-if="id === 'dino'">
      <path
        fill="currentColor"
        d="M2.382 8H1a1 1 0 0 1-.857-1.514C3.013 1.7 7.079-.154 11.403.512 14.755 1.028 18 3.19 18 5c0 .83.097.955.98 1.286.349.13 2.105.688 2.336.765 1.888.63 2.548 2.23 2.165 4.145-.262 1.308-1.04 2.777-1.774 3.511-.901.902-1.592.902-3.377.49-.611-.141-.957-.197-1.33-.197-2.657 0-4 2.15-4 7a1 1 0 0 1-1 1c-2.897 0-5.77-1.077-8.6-3.2a1 1 0 0 1-.294-1.247L4.382 16H3a1 1 0 0 1-.894-1.447L3.382 12H2a1 1 0 0 1-.894-1.447L2.382 8zm8.64 12.95C11.255 15.803 13.239 13 17 13c.564 0 1.03.075 1.78.248 1.103.254 1.303.254 1.513.045.453-.453 1.042-1.565 1.226-2.49.204-1.017-.03-1.586-.835-1.854-.186-.062-2.001-.639-2.405-.79C16.652 7.549 16 6.71 16 5c0-.524-2.406-2.128-4.902-2.512-3.051-.47-5.905.58-8.204 3.512H4a1 1 0 0 1 .894 1.447L3.618 10H5a1 1 0 0 1 .894 1.447L4.618 14H6a1 1 0 0 1 .894 1.447l-1.618 3.237c1.937 1.324 3.85 2.075 5.747 2.267z"
      />
    </template>
    <template v-else-if="id === 'slack'">
      <g
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        stroke="currentColor"
        fill="none"
      >
        <path
          d="M14.5 10c-.83 0-1.5-.67-1.5-1.5v-5c0-.83.67-1.5 1.5-1.5s1.5.67 1.5 1.5v5c0 .83-.67 1.5-1.5 1.5z"
        />
        <path
          d="M20.5 10H19V8.5c0-.83.67-1.5 1.5-1.5s1.5.67 1.5 1.5-.67 1.5-1.5 1.5z"
        />
        <path
          d="M9.5 14c.83 0 1.5.67 1.5 1.5v5c0 .83-.67 1.5-1.5 1.5S8 21.33 8 20.5v-5c0-.83.67-1.5 1.5-1.5z"
        />
        <path
          d="M3.5 14H5v1.5c0 .83-.67 1.5-1.5 1.5S2 16.33 2 15.5 2.67 14 3.5 14z"
        />
        <path
          d="M14 14.5c0-.83.67-1.5 1.5-1.5h5c.83 0 1.5.67 1.5 1.5s-.67 1.5-1.5 1.5h-5c-.83 0-1.5-.67-1.5-1.5z"
        />
        <path
          d="M15.5 19H14v1.5c0 .83.67 1.5 1.5 1.5s1.5-.67 1.5-1.5-.67-1.5-1.5-1.5z"
        />
        <path
          d="M10 9.5C10 8.67 9.33 8 8.5 8h-5C2.67 8 2 8.67 2 9.5S2.67 11 3.5 11h5c.83 0 1.5-.67 1.5-1.5z"
        />
        <path
          d="M8.5 5H10V3.5C10 2.67 9.33 2 8.5 2S7 2.67 7 3.5 7.67 5 8.5 5z"
        />
      </g>
    </template>
    <template v-else-if="id === 'rotate'">
      <g fill="none" stroke="currentColor" stroke-width="2">
        <polyline points="1 4 1 10 7 10" />
        <path d="M3.51 15a9 9 0 1 0 2.13-9.36L1 10" />
      </g>
    </template>
    <template v-else-if="id === 'expand'">
      <path
        fill="currentColor"
        d="M18.7 9.7c-.2.2-.4.3-.7.3-.3 0-.5-.1-.7-.3L12 4.4 6.7 9.7c-.4.4-1 .4-1.4 0-.4-.4-.4-1 0-1.4l6-6c.4-.4 1-.4 1.4 0l6 6c.4.4.4 1 0 1.4zm0 6l-6 6c-.2.2-.4.3-.7.3-.3 0-.5-.1-.7-.3l-6-6c-.4-.4-.4-1 0-1.4.4-.4 1-.4 1.4 0l5.3 5.3 5.3-5.3c.4-.4 1-.4 1.4 0 .4.4.4 1 0 1.4z"
      />
    </template>
    <template v-else-if="id === 'collapse'">
      <path
        fill="currentColor"
        d="M18.7 21.7c-.2.2-.4.3-.7.3-.3 0-.5-.1-.7-.3L12 16.4l-5.3 5.3c-.4.4-1 .4-1.4 0-.4-.4-.4-1 0-1.4l6-6c.4-.4 1-.4 1.4 0l6 6c.4.4.4 1 0 1.4zm0-18l-6 6c-.2.2-.4.3-.7.3-.3 0-.5-.1-.7-.3l-6-6c-.4-.4-.4-1 0-1.4.4-.4 1-.4 1.4 0L12 7.6l5.3-5.3c.4-.4 1-.4 1.4 0 .4.4.4 1 0 1.4z"
      />
    </template>
    <template v-else-if="id === 'edit'">
      <path
        fill="currentColor"
        d="M21 14.7V20c0 1.7-1.3 3-3 3H4c-1.7 0-3-1.3-3-3V6c0-1.7 1.3-3 3-3h5.3c.6 0 1 .4 1 1s-.4 1-1 1H4c-.6 0-1 .4-1 1v14c0 .6.4 1 1 1h14c.6 0 1-.4 1-1v-5.3c0-.6.4-1 1-1s1 .4 1 1zm1.7-8l-10 10c-.2.2-.4.3-.7.3H8c-.6 0-1-.4-1-1v-4c0-.3.1-.5.3-.7l10-10c.4-.4 1-.4 1.4 0l4 4c.4.4.4 1 0 1.4zM20.6 6L18 3.4l-9 9V15h2.6l9-9z"
      />
    </template>
    <template v-else-if="id === 'info'">
      <path
        fill="currentColor"
        d="M12 1C5.9 1 1 5.9 1 12s4.9 11 11 11 11-4.9 11-11S18.1 1 12 1zm0 20c-5 0-9-4-9-9s4-9 9-9 9 4 9 9-4 9-9 9zm1-9v4c0 .6-.4 1-1 1s-1-.4-1-1v-4c0-.6.4-1 1-1s1 .4 1 1zm-.3-4.7c.2.2.3.4.3.7 0 .3-.1.5-.3.7-.2.2-.4.3-.7.3h-.2c-.1 0-.1 0-.2-.1-.1 0-.1-.1-.2-.1s-.1-.1-.1-.1c-.2-.2-.3-.4-.3-.7 0-.3.1-.5.3-.7l.1-.1c.1 0 .1-.1.2-.1s.1 0 .2-.1c.3 0 .7.1.9.3z"
      />
    </template>
    <template v-else-if="id === 'cpg'">
      <path
        d="M20.9 7.6c-.1-.1-.1-.2-.2-.3l-6-6c-.1-.1-.2-.2-.3-.2-.1-.1-.3-.1-.4-.1H6C4.3 1 3 2.3 3 4v16c0 1.7 1.3 3 3 3h12c1.7 0 3-1.3 3-3V8c0-.1 0-.3-.1-.4zM15 4.4L17.6 7H15V4.4zM18 21H6c-.6 0-1-.4-1-1V4c0-.6.4-1 1-1h7v5c0 .6.4 1 1 1h5v11c0 .6-.4 1-1 1zm-1-8c0 .6-.4 1-1 1H8c-.6 0-1-.4-1-1s.4-1 1-1h8c.6 0 1 .4 1 1zm0 4c0 .6-.4 1-1 1H8c-.6 0-1-.4-1-1s.4-1 1-1h8c.6 0 1 .4 1 1zM7 9c0-.6.4-1 1-1h2c.6 0 1 .4 1 1s-.4 1-1 1H8c-.6 0-1-.4-1-1z"
        fill="currentColor"
        fill-rule="evenodd"
      />
    </template>
    <template v-else-if="id === 'faq'">
      <path
        d="M18.023 1.617a11.762 11.762 0 0 1 4.372 4.36C23.465 7.82 24 9.828 24 12c0 2.172-.535 4.18-1.605 6.023a11.85 11.85 0 0 1-4.372 4.372C16.18 23.465 14.172 24 12 24c-2.172 0-4.18-.535-6.023-1.605a11.85 11.85 0 0 1-4.372-4.372C.535 16.18 0 14.172 0 12c0-2.172.535-4.18 1.605-6.023a11.85 11.85 0 0 1 4.372-4.372C7.82.535 9.828 0 12 0c2.172 0 4.18.54 6.023 1.617zM15 1.945V6.82A5.837 5.837 0 0 1 17.18 9h4.875c-.25-.844-.602-1.64-1.055-2.39-.453-.75-.98-1.426-1.582-2.028A10.619 10.619 0 0 0 17.391 3 10.216 10.216 0 0 0 15 1.945zM16.5 12c0-.813-.203-1.562-.61-2.25a4.586 4.586 0 0 0-1.64-1.64A4.343 4.343 0 0 0 12 7.5c-1.234 0-2.293.441-3.176 1.324S7.5 10.766 7.5 12c0 .813.203 1.566.61 2.262a4.466 4.466 0 0 0 1.64 1.64A4.409 4.409 0 0 0 12 16.5c1.234 0 2.293-.437 3.176-1.313.883-.875 1.324-1.937 1.324-3.187zm-6-10.383v4.594C11.016 6.07 11.52 6 12.012 6s.988.07 1.488.21V1.618a9.703 9.703 0 0 0-3 0zM9 1.945c-1.047.313-2.031.79-2.953 1.43C4.016 4.765 2.648 6.641 1.945 9H6.82A6.082 6.082 0 0 1 9 6.82V1.945zM1.5 12c0 .469.04.969.117 1.5h4.57C6.063 13 6 12.5 6 12s.07-1 .21-1.5H1.618l-.047.375a6.08 6.08 0 0 0-.035.375l-.023.375A6.01 6.01 0 0 0 1.5 12zM9 22.055V17.18A5.837 5.837 0 0 1 6.82 15H1.945c.5 1.688 1.38 3.16 2.637 4.418A10.294 10.294 0 0 0 9 22.055zm4.5.328v-4.57c-.5.125-.996.187-1.488.187s-.996-.062-1.512-.188v4.57a9.702 9.702 0 0 0 3 0zm1.5-.328a10.147 10.147 0 0 0 3.105-1.512 10.413 10.413 0 0 0 2.426-2.438c.672-.945 1.18-1.98 1.524-3.105H17.18A5.837 5.837 0 0 1 15 17.18v4.875zm2.813-8.555h4.57c.078-.531.117-1.031.117-1.5 0-.469-.04-.969-.117-1.5h-4.594c.14.5.211 1 .211 1.5a6.041 6.041 0 0 1-.188 1.5z"
        fill="currentColor"
        fill-rule="evenodd"
      />
    </template>
    <template v-else-if="id === 'square'">
      <rect
        x="3"
        y="3"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        rx="2"
        width="18"
        height="18"
        ry="2"
      />
    </template>
    <template v-else-if="id === 'successSquare'">
      <path
        fill="currentColor"
        d="M19 2c1.7 0 3 1.3 3 3v14c0 1.7-1.3 3-3 3H5c-1.7 0-3-1.3-3-3V5c0-1.7 1.3-3 3-3h14zm-2.3 8.7c.4-.4.4-1 0-1.4-.4-.4-1-.4-1.4 0L11 13.6l-2.3-2.3c-.4-.4-1-.4-1.4 0-.4.4-.4 1 0 1.4l3 3c.2.2.4.3.7.3.3 0 .5-.1.7-.3l5-5z"
      />
    </template>
    <template v-else-if="id === 'external'">
      <path
        fill="currentColor"
        d="M19 13v6c0 1.7-1.3 3-3 3H5c-1.7 0-3-1.3-3-3V8c0-1.7 1.3-3 3-3h6c.6 0 1 .4 1 1s-.4 1-1 1H5c-.6 0-1 .4-1 1v11c0 .6.4 1 1 1h11c.6 0 1-.4 1-1v-6c0-.6.4-1 1-1s1 .4 1 1zm2.9-10.4c-.1-.2-.3-.4-.5-.5-.1-.1-.3-.1-.4-.1h-6c-.6 0-1 .4-1 1s.4 1 1 1h3.6l-9.3 9.3c-.4.4-.4 1 0 1.4.2.2.4.3.7.3.3 0 .5-.1.7-.3L20 5.4V9c0 .6.4 1 1 1s1-.4 1-1V3c0-.1 0-.3-.1-.4z"
      />
    </template>
    <template v-else-if="id === 'copy'">
      <g stroke="currentcolor" stroke-width="2" fill="none">
        <rect x="9" y="9" width="13" height="13" rx="2" ry="2" />
        <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1" />
      </g>
    </template>
    <template v-else-if="id === 'grid'">
      <g fill="none" stroke="currentColor" stroke-width="2">
        <rect x="3" y="3" width="7" height="7" />
        <rect x="14" y="3" width="7" height="7" />
        <rect x="14" y="14" width="7" height="7" />
        <rect x="3" y="14" width="7" height="7" />
      </g>
    </template>
    <template v-else-if="id === 'list'">
      <g fill="none" stroke="currentColor" stroke-width="2">
        <line x1="21" y1="10" x2="3" y2="10" />
        <line x1="21" y1="6" x2="3" y2="6" />
        <line x1="21" y1="14" x2="3" y2="14" />
        <line x1="21" y1="18" x2="3" y2="18" />
      </g>
    </template>
    <template v-else-if="id === 'zoom'">
      <path
        fill="currentColor"
        d="M23.5 6.1c-.3-.2-.7-.1-1 .1L17 10.1V7c0-1.7-1.3-3-3-3H3C1.3 4 0 5.3 0 7v10c0 1.7 1.3 3 3 3h11c1.7 0 3-1.3 3-3v-3.1l5.4 3.9c.2.1.4.2.6.2.2 0 .3 0 .5-.1.3-.2.5-.5.5-.9V7c0-.4-.2-.7-.5-.9zM15 17c0 .6-.4 1-1 1H3c-.6 0-1-.4-1-1V7c0-.6.4-1 1-1h11c.6 0 1 .4 1 1v10zm7-1.9L17.7 12 22 8.9v6.2z"
      />
    </template>
    <template v-else-if="id === 'idcard'">
      <g fill="none" fill-rule="evenodd">
        <path
          fill="currentColor"
          fill-rule="nonzero"
          d="M4 4h16a3 3 0 0 1 3 3v10a3 3 0 0 1-3 3H4a3 3 0 0 1-3-3V7a3 3 0 0 1 3-3zm0 2a1 1 0 0 0-1 1v10a1 1 0 0 0 1 1h16a1 1 0 0 0 1-1V7a1 1 0 0 0-1-1H4z"
        />
        <rect
          width="6"
          height="2"
          x="13"
          y="8"
          fill="currentColor"
          fill-rule="nonzero"
          rx="1"
        />
        <rect
          width="4"
          height="2"
          x="13"
          y="12"
          fill="currentColor"
          fill-rule="nonzero"
          rx="1"
        />
        <rect
          width="5"
          height="6"
          x="5"
          y="9"
          stroke="currentColor"
          stroke-width="2"
          rx="1"
        />
      </g>
    </template>
    <template v-else-if="id === 'moz'">
      <defs>
        <path id="a" d="M0 0h24v24H0z" />
      </defs>
      <g fill="none" fill-rule="evenodd">
        <path
          fill="currentColor"
          fill-rule="nonzero"
          d="M22.276 15.227H24V18h-5.436v-7.193c0-2.21-.752-3.034-2.21-3.034-1.768 0-2.476 1.257-2.476 2.99v4.42h1.724v2.774h-5.436v-7.15c0-2.21-.752-3.034-2.21-3.034-1.768 0-2.475 1.257-2.475 2.99v4.42h2.475v2.774H0v-2.774h1.724v-7.15H0V5.26h5.436v1.907C6.232 5.823 7.558 5 9.37 5c1.857 0 3.58.867 4.2 2.73C14.275 6.04 15.734 5 17.767 5c2.342 0 4.464 1.387 4.464 4.377v5.85h.044z"
        />
        <use fill="currentColor" fill-opacity="0" xlink:href="#a" />
      </g>
    </template>
    <template v-else-if="id === 'eye'">
      <defs>
        <path
          id="a"
          d="M23.925 11.6C23.725 11.2 19.515 3 12 3 4.484 3 .276 11.2.075 11.6c-.1.3-.1.6 0 .9.2.3 4.41 8.5 11.925 8.5 7.516 0 11.724-8.2 11.925-8.6.1-.2.1-.6 0-.8zM12 19c-5.411 0-8.919-5.4-9.92-7C2.98 10.4 6.588 5 12 5s8.919 5.4 9.92 7c-1.001 1.6-4.509 7-9.92 7zm0-11c-2.205 0-4.008 1.8-4.008 4S9.795 16 12 16s4.008-1.8 4.008-4S14.205 8 12 8zm0 6c-1.102 0-2.004-.9-2.004-2s.902-2 2.004-2c1.102 0 2.004.9 2.004 2s-.902 2-2.004 2z"
        />
      </defs>
      <g fill="none" fill-rule="evenodd">
        <mask id="b" fill="#fff">
          <use xlink:href="#a" />
        </mask>
        <use fill="#000" fill-rule="nonzero" xlink:href="#a" />
        <g fill="#000" mask="url(#b)">
          <path d="M0 0h24v24H0z" />
        </g>
      </g>
    </template>
    <template v-else-if="id === 'self-avatar'">
      <image
        v-if="avatarUrl"
        :href="avatarUrl"
        x="0"
        y="0"
        width="24"
        height="24"
      />
    </template>
  </svg>
</template>

<script>
import avatarUrl from '@/assets/js/avatars';
import generateIdenticon from '@/assets/js/identicon-avatar';

export default {
  name: 'Icon',
  props: {
    width: Number,
    height: Number,
    id: String,
  },
  mounted() {
    if (this.id === 'self-avatar') {
      if (this.$store.state.user.picture.value) {
        this.avatarUrl = avatarUrl(
          this.$store.state.user.picture.value,
          40,
          true,
        );
      } else {
        generateIdenticon(
          this.$store.state.user.primaryUsername.value,
          40,
        ).then((a) => {
          this.avatarUrl = a;
        });
      }
    }
  },
  data() {
    return {
      avatarUrl: null,
    };
  },
};
</script>
