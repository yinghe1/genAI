Install flowise https://github.com/FlowiseAI/Flowise low code Drag & drop UI to build your customized LLM flow
This file has steps to build the git cloned Flowise on the local machine. 
- Install node 20 https://nodejs.org/en/download on Mac it goes to /usr/local/lib/node_modules. I picked 20 because someone mentioned higher version flowise has issue
- when it complain about workspace because it needs pnpm
- Install pnpm https://pnpm.io/installation
- npm install --global corepack@latest
- corepack enable pnpm
- corepack use pnpm@latest-10
- Flowise use monorepo and packages folder has separate components in Flowise/packages/server change workspace to
  - "flowise-components": "file:../components",
  - "flowise-ui": "file:../ui",
  - run pnpm install then npm run build in each of the packages/server packages/components pacakges/ui 
- then at root run npm install —verbose 
- https://www.youtube.com/watch?v=PLuSfAkOHOA watch this to build a simple RAG agent using LLM
