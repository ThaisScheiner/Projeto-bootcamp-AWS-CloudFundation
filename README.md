# Projeto bootcamp Code Girls - AWS CloudFormation

O **AWS CloudFormation** é a espinha dorsal da automação na AWS. Ele transforma a gestão de infraestrutura de uma tarefa manual e propensa a erros em um processo de engenharia de software, trazendo previsibilidade, segurança e escalabilidade para o provisionamento de recursos na nuvem.

O CloudFormation materializa essa ideia através de **templates**, arquivos de texto em `YAML` ou `JSON` que servem como uma planta baixa detalhada e executável do seu ambiente. Este arquivo se torna a **única fonte da verdade**.

Nele, você não escreve um script com uma sequência de comandos dizendo "faça isso, depois faça aquilo". Em vez disso, você adota uma abordagem **declarativa**: você descreve o estado final desejado.

> Você declara: *"eu quero uma rede virtual com estas características, dois servidores web com esta configuração e um balanceador de carga distribuindo o tráfego entre eles"*.

É o trabalho do CloudFormation, como um mestre de obras inteligente, interpretar essa planta baixa e orquestrar a construção de tudo, na ordem correta, com todas as dependências resolvidas.

Quando você entrega essa planta baixa ao serviço, ele a utiliza para construir um **Stack**. Um Stack é mais do que apenas um amontoado de recursos; é um recipiente vivo, uma unidade de gerenciamento coesa. É aqui que a mágica da confiança acontece.

Se, durante a construção de dez recursos, o oitavo falhar por qualquer motivo — uma permissão faltante, um limite de serviço atingido —, o CloudFormation não abandona a obra pela metade. Ele inicia um processo de **rollback atômico**, demolindo cuidadosamente tudo o que já havia construído para aquele Stack. Isso garante que você nunca fique em um estado inconsistente e quebrado. Essa rede de segurança automática elimina o medo de experimentar e de fazer alterações, pois o pior cenário é simplesmente voltar ao estado estável anterior.

Para o profissional que gerencia ambientes críticos, o CloudFormation oferece ferramentas de maestria:

* **Change Sets:** Permitem que você veja uma prévia exata de tudo que será alterado, modificado ou até mesmo destruído antes de aplicar uma reforma em sua infraestrutura, transformando o medo do "apertar o botão" em uma decisão informada e segura.
* **Detecção de Desvio (Drift Detection):** Atua como um sistema de alarme, notificando você se alguém fez uma alteração manual no console, garantindo que sua planta baixa continue sendo o reflexo fiel da realidade.