# Robô Terrestre Híbrido Deliberativo-Reativo

Simulação 3D interativa de um robô móvel terrestre com controle híbrido (arquitetura AuRA: camada deliberativa + camada reativa), feita pra a disciplina de Aplicações de Robótica do PPCIC/CEFET-RJ.

**[Abrir a simulação](./index.html)** (ou pelo GitHub Pages, depois de publicado)

## O que é

O robô precisa chegar sozinho a um ponto fixo a 3 metros do início, em linha reta, mesmo com obstáculos no caminho. A camada deliberativa recalcula a rota até o alvo a cada ciclo; a camada reativa lê os sensores ultrassônicos e assume o controle na hora se detectar algo perto, desviando e depois recalculando o retorno pela posição real (não só desfazendo o giro).

A simulação roda em Three.js, no navegador, sem instalar nada. Tem:

- Cena 3D de uma sala de aula com o robô, obstáculos que você pode colocar clicando, câmera livre e câmera em primeira pessoa (visão do sensor frontal)
- Tutorial guiado passo a passo
- Painel com esquemático elétrico, vista física das ligações e o código-fonte do Arduino
- Modo simples (esconde a sala e mostra só o robô, o chão e os obstáculos)

## Arquivos

- `index.html` — a simulação inteira, autocontida (não depende de nenhum servidor ou CDN)
- `robo_tour.mp4` — vídeo curto do robô de perto, usado no tutorial

## Como testar localmente

Não precisa de build nem instalação. Só abrir o `index.html` num servidor local (funciona melhor assim do que abrindo o arquivo direto, por causa do vídeo):

```
npx serve .
```

## Base

Robô real: Arduino Uno, módulo L293D, 2 motores DC com encoder ótico, 4x sensor ultrassônico HC-SR04. Testado no Tinkercad Circuits. O código real (`codigo_robo.ino`) e o código da simulação implementam a mesma máquina de estados.

---

Rafael Pinto · Prof. João Quadros · CEFET/RJ, PPCIC
