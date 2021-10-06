<template>
  <!-- 클래스 바인딩 -->
  <ClassBinding />
  <br /><br />
  <!-- 조건부 렌더링 -->
  <ConditionRendering />
  <br /><br />
  <!-- 리스트 렌더링 -->
  <ListRendering />
  <br /><br />
  <!-- 이벤트 핸들링 -->
  <EventHandling />
  <br /><br />
  <!-- 이벤트 수식어 -->
  <EventModifier />
  <br /><br />
  <!-- 키 수식어 -->
  <KeyModifier />
  <br /><br />
  <!-- 폼 입력 바인딩 -->
  <FormInputBinding />
  <br /><br />
  <!-- 컴포넌트 기초 -->
  <ComponentFoundation />
  <br /><br />
  <!-- 컴포넌트 속성 상속 -->
  <ComponentInheritance />
  <br /><br />
  <ComponentEmit />
  <br /><br />
</template>

<script>

import ClassBinding from '~/components/ClassBinding'
import ConditionRendering from '~/components/ConditionRendering'
import ListRendering from '~/components/ListRendering'
import EventHandling from '~/components/EventHandling'
import EventModifier from '~/components/EventModifier'
import KeyModifier from '~/components/KeyModifier'
import FormInputBinding from '~/components/FormInputBinding'
import ComponentFoundation from '~/components/ComponentFoundation'
import ComponentInheritance from '~/components/ComponentInheritance'
import ComponentEmit from '~/components/ComponentEmit'

export default {
    components: {
      ClassBinding,
      ConditionRendering,
      ListRendering,
      EventHandling,
      EventModifier,
      KeyModifier,
      FormInputBinding,
      ComponentFoundation,
      ComponentInheritance,
      ComponentEmit
    },
    
}
</script>

