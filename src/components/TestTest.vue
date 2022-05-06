<template>
    <div style="padding: 100px; boarder: 1px solid #eee">
        {{ myName }}
        <br/>
        {{ myMessage }}
    </div>
</template>


<script>
export default {
    props: ['myName', 'myMessage']
}
</script>