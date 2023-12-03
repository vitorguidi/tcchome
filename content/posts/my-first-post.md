+++
title = 'Trabalho de conclusão de curso - MAC0499'
date = 2023-12-03T18:53:53-03:00
draft = false
+++

# Provendo alta disponibilidade ao sistema SPIRA com Kubernetes

Página para a disciplina MAC0499 - Trabalho de formatura supervisionado

**Aluno:** Vitor Guidi

**Orientador:** Prof. Dr. Alfredo Goldman

**Co-Orientador:** Me. Renato Cordeiro Ferreira

## Resumo

O SPIRA é um projeto de pesquisa na Universidade de São Paulo, cujo propósito é detectar insuficiência resporatória por meio de análise de voz, utilizando aprendizado de máquina. Em um projeto anterior, [Victor Tamae](https://daitamae.github.io/MAC0499/) desenvolveu um conjunto de microsserviços para possibilitar que o SPIRA seja utilizado em hospitais. Entretanto, por limitações de tempo, todos os microsserviços foram provisionados como uma única réplica, dentro de uma única máquina virtual. 

Esta estratégia de provisionamento não provê alta disponibilidade, já que o serviço inteiro pode ficar indisponível se uma réplica de um dos microsserviços parar de funcionar, ou se a máquina hospedeira ficar indisponível. 

O objetivo desta pesquisa é prover alta disponibilidade para os microsserviços do SPIRA, por meio da migração para o Kubernetes -- atualmente, o orquestrador de contêineres mais popular da indústria. Uma nova arquitetura de provisionamento foi proposta, que pode ser implantada em um conjunto de máquinas ao invés de uma única réplica. 

Finalmente, para verificar que de fato foi adicionada alta disponibilidade, esta pesquisa utilizou testes de caos para garantir que o sistema continue respondendo e não haja perda de dados quando diferentes réplicas dos microsserviços são desligadas aleatoriamente.

## Proposta

[Link para a proposta no github](https://github.com/vitorguidi/mac0499/blob/master/Proposta_TCC_Spira.pdf)

## Monografia

[Link para a monografia no github](https://github.com/vitorguidi/mac0499/blob/master/Monografia_tcc_spira.pdf)

## Repositórios relevantes

[Código gerado para provisionamento e testes do SPIRA no Kubernetes](https://github.com/vitorguidi/mac0499/tree/master)

[SPIRA API Server](https://github.com/spirabr/SPIRA-API)

[SPIRA Inference Server](https://github.com/spirabr/SPIRA-Inference-Service)