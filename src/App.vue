<template>
<div class="layer"></div>
<!-- ! Body -->
<a class="skip-link sr-only" href="#skip-target">Skip to content</a>
<div class="page-flex">
    <!-- ! Sidebar -->
    <aside class="sidebar">
        <div class="sidebar-start">
            <div class="sidebar-head">
                <a href="/" class="logo-wrapper" title="Home">
                    <span class="sr-only">Home</span>
                    <span class="icon logo" aria-hidden="true"></span>
                    <div class="logo-text">
                        <span class="logo-title">Vue JS</span>
                        <span class="logo-subtitle">Dashboard</span>
                    </div>

                </a>
                <button class="sidebar-toggle transparent-btn" title="Menu" type="button">
                    <span class="sr-only">Toggle menu</span>
                    <span class="icon menu-toggle" aria-hidden="true"></span>
                </button>
            </div>
            <div class="sidebar-body">
                <ul class="sidebar-body-menu">
                    <li>
                        <router-link to="/" class="{:active}">
                            <span class="icon home" aria-hidden="true"></span>Dashboard
                        </router-link>
                    </li>
                    <li>
                        <router-link to="/about">
                            <span class="icon user-3" aria-hidden="true"></span>Usuarios
                        </router-link>
                    </li>
                     <li>
                        <router-link to="/centeroperation">
                            <span class="icon home" aria-hidden="true"></span>Centros OP
                        </router-link>
                    </li>
                </ul>
                <ul class="sidebar-body-menu">
                    <li>
                        <a class="show-cat-btn" href="##">
                            <span class="icon category" aria-hidden="true"></span>Extentions
                            <span class="category__btn transparent-btn" title="Open list">
                                <span class="sr-only">Open list</span>
                                <span class="icon arrow-down" aria-hidden="true"></span>
                            </span>
                        </a>
                        <ul class="cat-sub-menu">
                            <li>
                                <router-link to="/about">Sobre Nosotros</router-link>
                            </li>
                        </ul>
                    </li>

                </ul>
            </div>
        </div>
        <div class="sidebar-footer">
            <a href="##" class="sidebar-user">
                <span class="sidebar-user-img">
                    <picture>
                        <source srcset="../src/assets/img/avatar/avatar-illustrated-01.webp" type="image/webp"><img src="../src/assets/img/avatar/avatar-illustrated-01.png" alt="User name"></picture>
                </span>
                <div class="sidebar-user-info">
                    <span class="sidebar-user__title">Nafisa Sh.</span>
                    <span class="sidebar-user__subtitle">Support manager</span>
                </div>
            </a>
        </div>
    </aside>
    <div class="main-wrapper">
        <!-- ! Main nav -->
        <nav class="main-nav--bg">
            <div class="container main-nav">
                <div class="main-nav-start">
                    <div class="search-wrapper">
                        <i data-feather="search" aria-hidden="true"></i>
                        <input type="text" placeholder="Enter keywords ..." required>
                    </div>
                </div>
                <div class="main-nav-end">
                    <button class="sidebar-toggle transparent-btn" title="Menu" type="button">
                        <span class="sr-only">Toggle menu</span>
                        <span class="icon menu-toggle--gray" aria-hidden="true"></span>
                    </button>   
                    <button class="theme-switcher gray-circle-btn" type="button" title="Switch theme">
                        <span class="sr-only">Switch theme</span>
                        <i class="sun-icon" data-feather="sun" aria-hidden="true"></i>
                        <i class="moon-icon" data-feather="moon" aria-hidden="true"></i>
                    </button>       
                    <div class="nav-user-wrapper">
                        <button href="##" class="nav-user-btn dropdown-btn" title="My profile" type="button">
                            <span class="sr-only">My profile</span>
                            <span class="nav-user-img">
                                <picture>
                                    <source srcset="../src/assets/img/avatar/avatar-illustrated-02.webp" type="image/webp"><img src="../src/assets/img/avatar/avatar-illustrated-02.png" alt="User name"></picture>
                            </span>
                        </button>
                        <ul class="users-item-dropdown nav-user-dropdown dropdown">
                            <li>
                                <a href="##">
                                    <i data-feather="user" aria-hidden="true"></i>
                                    <span>Profile</span>
                                </a>
                            </li>
                            <li>
                                <a href="##">
                                    <i data-feather="settings" aria-hidden="true"></i>
                                    <span>Account settings</span>
                                </a>
                            </li>
                            <li>
                                <a class="danger" href="##">
                                    <i data-feather="log-out" aria-hidden="true"></i>
                                    <span>Log out</span>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </nav>
        <!-- ! Main -->
        <main class="main users chart-page" id="skip-target">
            <div class="container">
                <router-view />
            </div>
        </main>
        <!-- ! Footer -->
        <footer class="footer">
            <div class="container footer--flex">
                <div class="footer-start">
                    <p>2021 © Luifer Almendrales - <a href="https://luifer1994.github.io" target="_blank" rel="noopener noreferrer">luifer1994.github.io</a></p>
                </div>
            </div>
        </footer>
    </div>
</div>
</template>

<style>
a.router-link-exact-active {
    color: #ffffff;
    font-weight: bold;
    border-radius: 10px;
    background-color: rgba(255, 255, 255, 0.308);
    padding: 5px;
}
</style>
