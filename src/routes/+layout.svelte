<script lang='ts'>
  import "../app.postcss"
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger,  Footer, FooterBrand, FooterCopyright, FooterLinkGroup, FooterLink, Hr } from 'flowbite-svelte'
</script>

<Navbar let:hidden let:toggle>
  <NavBrand href="/">
    <img
      src="https://flowbite-svelte.com/images/flowbite-svelte-icon-logo.svg"
      class="mr-3 h-6 sm:h-9"
      alt="Flowbite-Svelte Logo"
    />
    <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
      Flowbite-Svelte
    </span>
  </NavBrand>
  <NavHamburger on:click={toggle} />
  <NavUl {hidden}>
    <NavLi href="/" active={true}>Home</NavLi>
  </NavUl>
</Navbar>
<main class='p-8 h-auto'>
  <slot />
</main>

<Footer footerType="logo" class='p-8'>
  <div class="sm:flex sm:items-center sm:justify-between">
    <FooterBrand
      href="https://flowbite-svelte.com"
      src="https://flowbite-svelte.com/images/flowbite-svelte-icon-logo.svg"
      alt="Flowbite Logo"
      name="Flowbite"
    />
    <FooterLinkGroup ulClass="flex flex-wrap items-center mb-6 text-sm text-gray-500 sm:mb-0 dark:text-gray-400">
      <FooterLink href="/">About</FooterLink>
      <FooterLink href="/">Privacy Policy</FooterLink>
      <FooterLink href="/">Licensing</FooterLink>
      <FooterLink href="/">Contact</FooterLink>
    </FooterLinkGroup>
  </div>
  <Hr class="my-6" height="h-px" />
  <FooterCopyright href="/" by="Flowbite-Svelte™" />
</Footer>