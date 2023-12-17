<template>
    <div class="navbar">
        <div class="navbar-contents">
            <div class="navbar-name">
                <a href="#app" class="my-name">{{ myName }}</a>
            </div>
            <div class="navbar-links">
                <a href="#AboutMe" class="navbar-link">About Me</a>
                <a href="#MyProjects" class="navbar-link">Projects</a>
                <button class="cv-btn">Download CV</button>
            </div>
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
@media screen and (max-width: 768px) {

    .navbar-contents {
        flex-direction: column;
        align-items: center;
        display: flex;
        margin-right: 100px;
        justify-content: space-between;
        background-color: #1f2021;
        color: white;
        padding: 10px 20px;
        font-family: 'CustomFont', 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    }

    .navbar-links {
        align-items: center;
        margin-left: 50px;
        display: flex;
    }

    .navbar-link {
        font-size: 14px;
        padding: 6px 10px;
        margin-left: 25px;
        white-space: nowrap;
    }

    .navbar-name {
        margin: 0;
        margin-bottom: 15px;
    }

    .cv-btn {
        white-space: nowrap;
    }
}

.navbar {
    background-color: #1f2021;
    margin-bottom: 10px;
}

.navbar-contents {
    display: flex;
    margin-right: 100px;
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
    margin-left: 100px;
    color: #bbc9bf;
    cursor: pointer;
}

.my-name {
    text-decoration: none;
    color: inherit;
}

.cv-btn {
    padding: 8px 16px;
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