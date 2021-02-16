---
title: Restrições do Address Book
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432797"
---
# <a name="address-book-restrictions"></a>Restrições do Address Book

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de agendas são necessários para dar suporte a três tipos de restrições nos índices de conteúdo de seus contêineres:
  
- Restrições de propriedade de nome ambíguo
    
- Restrições de propriedade de chave de instância
    
- Restrições de conteúdo de nome de exibição prefixados
    
Restrições de nome ambíguas são restrições de propriedade usando a **propriedade PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para corresponder nomes de destinatários com entradas em contêineres de livro de endereços. A **PR_ANR** restrição de propriedade é um tipo de "melhor suposição" de pesquisa pelo qual os provedores de agendas de endereços podem escolher a propriedade correspondente que funciona melhor para seu contêiner. Por exemplo, um provedor de agendas de endereços pode implementar PR_ANR restrição correspondendo **nomes** de **destinatários** à propriedade PR_ACCOUNT ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contêiner, enquanto outro provedor pode usar **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
O MAPI recomenda que as implementações da restrição **de PR_ANR** equilibrem entre o desempenho adequado e a satisfação do usuário. A satisfação do usuário pode ser comprometida quando um provedor de agendas implementa a restrição de forma que muitas ou muitas combinações sejam encontradas. Alguns provedores de agendas de endereço suportam o que é conhecido como um nome distinto, ou comum, que não é exibido em uma caixa de diálogo, mas pode corresponder a uma restrição de nome ambígua. 
  
Uma implementação típica pode ser analisar o nome de exibição do destinatário em palavras, correspondendo a qualquer entrada que contenha todas as palavras. Atenção aos detalhes, como sensibilidade à posição da palavra, se palavras não seguras são acionadas e a escolha de caracteres separadores pode variar. Por exemplo, se o nome a ser resolvido  for "Bill L", uma restrição PR_ANR comum selecionará as seguintes entradas como correspondentes: 
  
- Dra.
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Restrições de chave de instância ou **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) são usadas na implementação de caixas de listagem que são usadas em aplicativos cliente para exibir tabelas MAPI. Algumas implementações de caixa de listagem permitem que os usuários façam várias seleções, rolem para cima ou para baixo e retornem ao primeiro item selecionado. Para implementar esse comportamento, os clientes chamam [IMAPITable::FindRow](imapitable-findrow.md), passando uma restrição de propriedade na propriedade **PR_INSTANCE_KEY** para o método. Os provedores de agendas são necessários para dar suporte a essa restrição. 
  
Outro recurso de caixas de listagem usadas para exibição de tabela é a capacidade de posicionar o cursor com base em um conjunto de caracteres de prefixo. À medida que o usuário começa a digitar caracteres de prefixo, o cliente move o cursor para o primeiro item que começa com esses caracteres. Os clientes implementam esse recurso com uma restrição de conteúdo com **base na propriedade PR_DISPLAY_NAME** e no nível FL_PREFIX difusa. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

