<script lang="ts">
  import {
    MegaMenu,
    MegaMenuWithExtraList,
  } from '@employee-dashboard/web/components';
  import {
    MenuDashboard,
    MenuEmployees,
    MenuProjects,
    UserImage,
  } from '@employee-dashboard/web/assets';

  const links = [
    {
      image: MenuDashboard,
      title: 'Dashboard',
      subtitle: 'See your dashboard',
      url: '/',
    },

    {
      image: MenuProjects,
      title: 'Projects',
      subtitle: 'Manage your projects',
      url: '/projects',
    },

    {
      image: MenuEmployees,
      title: 'Employees',
      subtitle: 'Manage your employees',
      url: '/employees',
    },
  ];

  const menu = ['Employee', 'Projects', 'Clients', 'About'];
</script>

<ul class="flex justify-center items-center gap-3 h-full">
  <li class="h-full flex items-center rounded-lg group relative">
    <p
      class="mx-3 hover:no-underline text-gray-800 dark:text-gray-200 group-hover:text-gray-400"
    >
      Add
    </p>
    <MegaMenuWithExtraList {links} extraLinks={links} />
  </li>
  {#each menu as item}
    <li class="h-full flex items-center rounded-lg group relative">
      <p
        class="mx-3 hover:no-underline text-gray-800 dark:text-gray-200 group-hover:text-gray-400"
      >
        {item}
      </p>
      <MegaMenu {links} />
    </li>
  {/each}
</ul>
