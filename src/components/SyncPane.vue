<template>
      <Card style="min-height:300px;">
            <template #title>
                Advanced Card
            </template>
            <template #subtitle>
                Card subtitle
            </template>
            <template #content>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Inventore sed consequuntur error repudiandae numquam deserunt
                quisquam repellat libero asperiores earum nam nobis, culpa ratione quam perferendis esse, cupiditate neque quas!</p>
            </template>
            <template #footer>
                <VideoSelectorControlPane />
            </template>
        </Card>
</template>

<script>
import Card from 'primevue/card';
import VideoSelectorControlPane from './VideoSelectorControlPane'
export default {
  name: 'OnboardingPane',
  components: {Card, VideoSelectorControlPane},
}
</script>

<style scoped>
p {
    line-height: 1.5;
    margin: 0;
}
</style>