<script lang="ts">
	import Dropdown from './dropdown.svelte';
	import NavbarEntry from './navbar_entry.svelte';
</script>

<nav
	class="group w-full min-h-16 font-sans flex justify-around hover:bg-mainhb transition duration-300 ease-in-out"
>
	<div class="hidden md:block" />
	<div class="text-sm gap-3 md:text-lg md:gap-6 flex place-content-end p-3 py-4">
		<NavbarEntry path="/" name="HOME">
			<svg fill="currentColor" slot="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" width=20 height=20>
        <!-- ! Font Awesome Free 6.0.0-beta3 by @fontawesome - https://fontawesome.com License -https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2021 Fonticons, Inc. -->
        <path
					d="M575.8 255.5C575.8 273.5 560.8 287.6 543.8 287.6H511.8L512.5 447.7C512.5 450.5 512.3 453.1 512 455.8V472C512 494.1 494.1 512 472 512H456C454.9 512 453.8 511.1 452.7 511.9C451.3 511.1 449.9 512 448.5 512H392C369.9 512 352 494.1 352 472V384C352 366.3 337.7 352 320 352H256C238.3 352 224 366.3 224 384V472C224 494.1 206.1 512 184 512H128.1C126.6 512 125.1 511.9 123.6 511.8C122.4 511.9 121.2 512 120 512H104C81.91 512 64 494.1 64 472V360C64 359.1 64.03 358.1 64.09 357.2V287.6H32.05C14.02 287.6 0 273.5 0 255.5C0 246.5 3.004 238.5 10.01 231.5L266.4 8.016C273.4 1.002 281.4 0 288.4 0C295.4 0 303.4 2.004 309.5 7.014L564.8 231.5C572.8 238.5 576.9 246.5 575.8 255.5L575.8 255.5z"
				/>
			</svg>
    </NavbarEntry>

		<Dropdown name="PROJEKTE">
			<svg fill="currentColor" slot="img1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" width=20 height=20>
        <!--! Font Awesome Free 6.0.0-beta3 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2021 Fonticons, Inc.-->
        <path 
          d="M464 96h-192l-64-64h-160C21.5 32 0 53.5 0 80V160h512V144C512 117.5 490.5 96 464 96zM0 432C0 458.5 21.5 480 48 480h416c26.5 0 48-21.5 48-48V192H0V432z"
        />
      </svg>
      <svg fill="currentColor" slot="img2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" width=20 height=20>
        <!--! Font Awesome Free 6.0.0-beta3 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2021 Fonticons, Inc.-->
        <path 
        d="M147.8 192H480V144C480 117.5 458.5 96 432 96h-160l-64-64h-160C21.49 32 0 53.49 0 80v328.4l90.54-181.1C101.4 205.6 123.4 192 147.8 192zM543.1 224H147.8C135.7 224 124.6 230.8 119.2 241.7L0 480h447.1c12.12 0 23.2-6.852 28.62-17.69l96-192C583.2 249 567.7 224 543.1 224z"
        />
      </svg>

			<div slot="dropcontent">
				<NavbarEntry path="/ " name="Messenger (coming soon)">
					<svg fill="currentColor"  slot="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" width=20 height=20>
            <!--! Font Awesome Free 6.0.0-beta3 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2021 Fonticons, Inc.-->
            <path 
              d="M256 0v128h128L256 0zM224 128L224 0H48C21.49 0 0 21.49 0 48v416C0 490.5 21.49 512 48 512h288c26.51 0 48-21.49 48-48V160h-127.1C238.3 160 224 145.7 224 128z"
            />
          </svg>
				</NavbarEntry>
				<NavbarEntry path="/ " name="Coming soon">
					<svg fill="currentColor"  slot="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" width=20 height=20>
            <!--! Font Awesome Free 6.0.0-beta3 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2021 Fonticons, Inc.-->
            <path 
              d="M256 0v128h128L256 0zM224 128L224 0H48C21.49 0 0 21.49 0 48v416C0 490.5 21.49 512 48 512h288c26.51 0 48-21.49 48-48V160h-127.1C238.3 160 224 145.7 224 128z"
            />
          </svg>
				</NavbarEntry>
			</div>
		</Dropdown>

		<NavbarEntry path="/impressum" name="IMPRESSUM">
			<svg fill="currentColor"  slot="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" width=20 height=20>
        <!--! Font Awesome Free 6.0.0-beta3 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2021 Fonticons, Inc.-->
        <path 
          d="M224 256c70.7 0 128-57.31 128-128s-57.3-128-128-128C153.3 0 96 57.31 96 128S153.3 256 224 256zM274.7 304H173.3C77.61 304 0 381.6 0 477.3c0 19.14 15.52 34.67 34.66 34.67h378.7C432.5 512 448 496.5 448 477.3C448 381.6 370.4 304 274.7 304z"
        />
      </svg>
		</NavbarEntry>
	</div>
</nav>
