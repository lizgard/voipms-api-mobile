<template>
    <Page>
        <ActionBar title="VoIP.ms API Setting"/>
        <TabView :selectedIndex="selectedIndex" @selectedIndexChange="indexChange">
            <TabViewItem title="Tab 1">
                <GridLayout columns="*" rows="*">
                    <Label class="message" :text="msg" col="0" row="0"/>
                </GridLayout>
            </TabViewItem>

            <TabViewItem title="Tab 2">
                <Label text="Content for Tab 2" />
            </TabViewItem>
        </TabView>
    </Page>
</template>

<script lang="ts">
  export default {
    data() {
      return {
        msg: 'El comunismo por el bien de todos'
      }
    },

    methods: {
        indexChange (args): void {
            let newIndex = args.value;
            console.log('Current tab index: ' + newIndex);
        }
    }
  }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }

    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>
