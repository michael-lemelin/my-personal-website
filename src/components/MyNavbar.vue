<template>
    <div class="navbar">
        <div class="navbar-name">
            <span class="my-name">{{ myName }}</span>
        </div>
        <div class="navbar-links">
            <router-link to="/AboutMe" class="navbar-link">About Me</router-link>
            <router-link to="/MyProjects" class="navbar-link">Projects</router-link>
            <button class="cv-btn">Download CV</button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            myName: "Michael Lemelin",
        }
    },
}
</script>

<style>
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #1f2021;
    color: white;
    padding: 10px 20px;
    font-family: 'CustomFont', 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.navbar-link {
    margin-right: 20px;
}

.navbar-name {
    font-size: 1.5rem;
    margin-left: 50px;
}

.cv-btn {
    padding: 8px 16px;
    margin-right: 50px;
    background-color: #5f7a66;
    border: none;
    color: #1f2021;
    border-radius: 2px;
    cursor: pointer;
    font-family: 'CustomFont', 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-size: 1.0rem;
    transition: transform 0.3s ease;
}

.cv-btn:hover {
    transform: scale(1.1);
}
</style>