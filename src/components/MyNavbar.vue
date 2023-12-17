<template>
    <div class="navbar">
        <div class="navbar-name">
            <a href="#app" class="my-name">{{ myName }}</a>
        </div>
        <div class="navbar-links">
            <a href="#AboutMe" class="navbar-link">About Me</a>
            <a href="#MyProjects" class="navbar-link">Projects</a>
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
    text-decoration: none;
    color: inherit;
    margin-right: 20px;
    cursor: pointer;
}

.navbar-name {
    font-size: 1.8rem;
    margin-left: 50px;
    color: #bbc9bf;
    cursor: pointer;
}

.my-name {
    text-decoration: none;
    color: inherit;
}

.cv-btn {
    padding: 8px 16px;
    margin-right: 50px;
    background-color: #bbc9bf;
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