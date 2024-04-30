<template>
    <nav class="navigation">
        <h2>Menu</h2>
        <div class="menu">
            <ul id="links">
                <li v-for="{ id, name, isSelected } in links" :key="id" :class="['link-button', {'border-left-selected': isSelected}]">{{ name }}</li>
            </ul>

            <div class="buttons">
                <p>Log out</p>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: "NavPages",
    data() {
        return {
            links: [
                { id: 1, name: "Home", url: "/", isSelected: true },
                { id: 2, name: "Carteira", url: "/wallet", isSelected: false },
                { id: 3, name: "Estatística", url: "/statistic", isSelected: false },
                { id: 4, name: "Mensagens", url: "/message", isSelected: false },
            ]
        }
    }
}
</script>

<style scoped>
.navigation {
    background-color: #030202;
    color: #f1f1f1;
    width: 300px;
    height: 100vh;
}

.menu {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 94%;
}

.buttons {
    margin: 24px;
    padding: 48px 24px;
    border-top: 1px solid #80808033;
}

h2 {
    margin-top: 24px;
}

.link-button {
    list-style-type: none;
    text-align: left;
    padding: 12px 24px;
    transition: all 0.2s;
    cursor: pointer;

    &:hover {
        background-color: #f1f1f1;
        color: #030303;
        font-weight: bold;
    }
}

.border-left-selected {
    border-left: 4px solid white;
}

#links {
    margin-top: 24px;
    display: flex;
    flex-direction: column;
    gap: 12px;
}
</style>