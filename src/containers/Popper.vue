<template>
    <div class="container">
        <h3>Popper 组件</h3>
        <br>
        <span>
            @placement:
            <pre>top, right, bottom, left</pre>
            <pre>(top|right|bottom|left)-start</pre>
            <pre>(top|right|bottom|left)-end</pre> @trigger:
            <pre>click/hover</pre> @hideWhenClickOutside:
            <pre>true/false</pre>

            @trigger: click, hover, focus         
        </span>
        <d-popper :hideWhenClickOutside="true">
            <template slot="content">
                <div>Hello World</div>
            </template>
            <d-button>click</d-button>
        </d-popper><br><br>
        <d-popper trigger="hover" placement="top-start">
            <template slot="content">
                <div>Hello World</div>
            </template>
            <d-button>hover</d-button>
        </d-popper>
        <br><br>
        <d-popper trigger="hover" :show-arrow="true" placement="top-end" title="title" content="content here" :appendToBody="true">
            <a>hover me</a>
        </d-popper>
        <d-popper trigger="click" :show-arrow="true" :placement="placement" title="title" content="content here" :appendToBody="true">
            <d-button>click me</d-button>
        </d-popper>
        <d-popper trigger="focus" :placement="placement" title="title" content="content here" :appendToBody="true">
            <d-button>focus</d-button>
        </d-popper>
    </div>
</template>
<script>
export default {
    data() {
        return {
            placement: 'bottom'
        }
    },
    created(){
        window.VM = this;
    }
}
</script>
