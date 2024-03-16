<script setup>
import SkillChip from "./components/SkillChip.vue";
import WorkCard from "./components/WorkCard.vue";

const skills = ['VueJs', 'Vue2', 'Vue3', 'Javascript', 'NodeJS', 'Typescript', 'Vite', 'Vuex', 'Pinia', 'Jest', 'Vuetify', 'Quasar', 'HTML5', 'CSS', 'SCSS', 'SASS'];
const secondary = ['Git', 'npm', '(yarn/pnpm)', 'Webpack', 'Babel', 'Responsive Design', 'SSR', 'ESR', 'PWA', 'TDD', 'Agile', 'Jira/Confluence', 'ClickUp', 'VSCode', 'Webstorm',]

const jobs = [
  {
    title: 'SenseHawk, Inc',
    position: 'Senior Software Engineer',
    description: 'Module owner. Development of the owned module, integration with other modules, prototyping, planning, components development, development and integration of new features, working with a product and design teams, support of the product.',
    startDate: 'October 2022',
    endDate: 'Feb 2024',
    linkedinLink: 'https://www.linkedin.com/company/sensehawk'
  },
  {
    title: 'IntexSoft',
    position: 'Software Engineer, Senior Software Engineer',
    description: 'Variety of different projects, mostly commercial web applications. Several big projects including NFT market platform. Working with different teams, leading a team at some point.',
    startDate: 'September 2020',
    endDate: 'October 2022',
    linkedinLink: 'https://www.linkedin.com/company/intexsoft'
  },
  {
    title: 'INSPR',
    position: 'Software Engineer',
    description: 'Fullstack development of the framework based on React library',
    startDate: 'October 2019',
    endDate: 'September 2020',
    linkedinLink: 'https://www.linkedin.com/company/insprlabs'
  }
]
</script>

<template>
  <div class="page">
    <div class="main-info ta-start">
      <div class="title">
        <h1 style="margin: 0;">
          Maksim Budzko
        </h1>
        <h2>Senior Software Engineer</h2>
      </div>
      <div>
        <h3>
          Summary
        </h3>
        <p>
          Results-oriented senior software engineer with over 4 years of experience specialising in front-end development.
          Skilled in VueJs, JavaScript, HTML, and CSS, with a strong problem-solving ability.
          Currently working as a senior-level developer at SenseHawk Inc, responsible for a module of a commercial solar application.
          Proven track record of successfully delivering projects across various domains, including mobile PWAs, NFT platform, and small commercial web apps.
        </p>
      </div>

      <div>
        <h3>
          Skills
        </h3>
        <div style="padding-left: 1rem;">
          <h5 style="margin-bottom: 0;">
            Primary
          </h5>
          <SkillChip
            v-for="skill in skills"
            :key="skill"
            :label="skill"
          />
        </div>

        <div style="padding-left: 1rem;">
          <h5 style="margin-bottom: 0;">
            Methodologies and other
          </h5>
          <SkillChip
            v-for="skill in secondary"
            :key="skill"
            :label="skill"
          />
        </div>
      </div>

      <div>
        <h3>
          Experience
        </h3>
        <div>
          <WorkCard
            v-for="job in jobs"
            :key="job.title"
            :title="job.title"
            :position="job.position"
            :description="job.description"
            :start-date="job.startDate"
            :end-date="job.endDate"
            :linkedin-link="job.linkedinLink"
          />
        </div>
      </div>

      <div>
        <h3> Education </h3>

        <div class="education">
          <div class="education__period">
            2017 - 2021
          </div>
          <div>
            <h5>
              Bachelor of Computer Science
            </h5>
            Yanka Kupala State University of Grodno: Mathematics and Informatics faculty, Computer Security.
          </div>
        </div>
      </div>
    </div>
    <div class="secondary-info ta-start">
      <div>
        <h4>
          Contacts
        </h4>
        <div class="subtitle">
          <div>
            Address: Poland, Wroclaw
          </div>
          <div>
            Phone:
            <a href="tel:+48698737515">
              +48698737515
            </a>
          </div>
          <div>
            Email:
            <a href="mailto:budzkomaksim@gmail.com">
              budzkomaksim@gmail.com
            </a>
          </div>
        </div>

        <h4>
          Links
        </h4>
        <div>
          <div>
            Github: <a
              href="https://github.com/mbudzko/"
              target="_blank"
            > https://github.com/mbudzko </a>
          </div>
          <div>
            LinkedIn: <a
              href="https://www.linkedin.com/in/maksim-budzko-388577219/"
              target="_blank"
            > maksim-budzko-388577219 </a>
          </div>
          <div>
            CV Repository: <a
              href="https://github.com/mbudzko/mbudzko_CV"
              target="_blank"
            > Click! </a>
          </div>
        </div>
      </div>

      <div class="remark">
        <div>
          This CV is a small VueJs app
        </div>
        <div>
          Check out web version <a
            href="https://mbudzko.github.io/mbudzko_CV/"
            target="_blank"
          >here</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
a {
  font-weight: 500;
}

.ta-start {
  text-align: start;
}
.page {
  width: 100%;
  display: grid;
  grid-template-columns: 65% auto;
}
.main-info {
  padding-right: 1rem;
}

.secondary-info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  position: fixed;
  right: 0;
  bottom: 0;
  top: 0;
  border-left: 1px solid #464646;
  padding: 2rem;
  margin: 1rem;
  height: auto;
}

.education {
  display: flex;
  justify-content: space-between;
  align-items: start;

  &__period {
    margin-right: 1rem;
    white-space: nowrap;
  }

  h5 {
    margin-top: 0;
    margin-bottom: 0.5rem;
  }
}

.remark {
  display: flex;
  flex-direction: column;
}

@media screen and (max-width: 900px) {
  .page {
    display: flex;
    flex-direction: column;
  }

  .secondary-info {
    border-left: none;
    border-top: 1px solid;
    margin: 1rem 0;
    padding: 1rem 0;
    position: relative;
    bottom: 0;
  }
}
</style>
