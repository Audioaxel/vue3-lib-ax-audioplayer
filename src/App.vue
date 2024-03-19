<script setup lang="ts">
import AXPlayer from '@lib/components/AXPlayer.vue';
import { ref } from 'vue';
import { AXGap, AXGlobalStyle, AXSection, AXText } from 'vue3-lib-ax-basics';

const showPlayerMenu = ref(false);

</script>

<template>
  <AXGlobalStyle>
    <header>
      <AXSection
        label="Just a simple header"
        label-size="medium"
        hide-divider
      >
    </AXSection>
    </header>
  
    <main>
      <AXSection
        label="Test Section"
        label-size="giant"
        min-height="100vh"
        style="background-color: hsl(var(--primary-color-hsl), 0.2);"
      >
        <AXGap :gap-props="{
          vertical: true,
          justify: 'center',
          align: 'center',
          size: 'large'
        }"
        style="padding: 24px;"
        >
          <h4>Jo Bruder</h4>
          <AXText>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Expedita facere vero minus necessitatibus magnam consequuntur molestias, deserunt repellendus est obcaecati quae tenetur consectetur debitis aliquam accusamus, illo neque, rem adipisci qui! Reprehenderit blanditiis quis incidunt, quisquam voluptate atque sint velit aperiam temporibus non doloribus inventore, dolore hic nihil veritatis error!
          </AXText>
          <h4>Jo Sister</h4>
          <AXText>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda dolor vel voluptas iste repudiandae nobis amet quo deserunt sunt nam.
          </AXText>
          Test: {{ showPlayerMenu }}
        </AXGap>
      </AXSection>
    </main>
    <footer>
      <AXSection
        label="Just a simple footer"
        label-size="medium"
        hide-divider
      >
      </AXSection>
    </footer>
    <AXPlayer>
      <template #icon>
        <img src="./assets/logo-color-white.svg" />
      </template>
    </AXPlayer>
  </AXGlobalStyle>
</template>