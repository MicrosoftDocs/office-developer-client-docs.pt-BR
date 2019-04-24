---
title: Restrições do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328074"
---
# <a name="address-book-restrictions"></a>Restrições do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de catálogos de endereços são necessários para dar suporte a três tipos de restrições nas tabelas de conteúdo de seus contêineres:
  
- Restrições de propriedade de nome ambíguo
    
- Restrições de propriedade de chave de instância
    
- Restrições de conteúdo do nome de exibição prefixado
    
Restrições de nome ambíguo são restrições de propriedade usando a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para corresponder os nomes de destinatários com entradas nos contêineres do catálogo de endereços. A restrição de propriedade **PR_ANR** é um tipo de "melhor palpite" de pesquisa em que os provedores de catálogo de endereços podem escolher a propriedade correspondente que funciona melhor para o seu contêiner. Por exemplo, um provedor de catálogo de endereços pode implementar a restrição **PR_ANR** por meio da correspondência de nomes de destinatários em relação à propriedade **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contêiner, enquanto outro provedor pode usar **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI recomenda que as implementações da restrição **PR_ANR** tenha um equilíbrio entre o desempenho adequado e a satisfação do usuário. A satisfação do usuário pode ser comprometida quando um provedor de catálogo de endereços implementa a restrição de tal forma que poucas ou muitas correspondências são encontradas. Alguns provedores de catálogos de endereços dão suporte a o que é conhecido como um nome distinto, ou comum, que não é exibível em uma caixa de diálogo, mas pode corresponder a uma restrição de nome ambíguo. 
  
Uma implementação típica pode ser analisar o nome de exibição do destinatário em palavras, correspondendo a qualquer entrada que contenha todas as palavras. Atenção aos detalhes, como confidencialidade para a posição da palavra, se as palavras não-consecutivas são atendidas e a opção de caracteres separadores podem variar. Por exemplo, se o nome a ser resolvido for "Bill L", uma restrição **PR_ANR** típica selecionaria as seguintes entradas como correspondência: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
As restrições de chave de instância ou as restrições de propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) são usadas na implementação das caixas de listagem usadas em aplicativos cliente para exibir tabelas MAPI. Algumas implementações de caixa de listagem permitem que os usuários façam várias seleções, role para cima ou para baixo e retorne ao primeiro item selecionado. Para implementar esse comportamento, os clientes chamam imApitable [:: FindRow](imapitable-findrow.md), passando uma restrição de propriedade na propriedade **PR_INSTANCE_KEY** para o método. Os provedores de catálogos de endereços são necessários para dar suporte a essa restrição. 
  
Outro recurso das caixas de listagem usadas para exibição de tabela é a capacidade de posicionar o cursor com base em um conjunto de caracteres de prefixo. À medida que o usuário começa a digitar os caracteres de prefixo, o cliente move o cursor para o primeiro item que começa com esses caracteres. Os clientes implementam esse recurso com uma restrição de conteúdo com base na propriedade **PR_DISPLAY_NAME** e no nível de fuzzing FL_PREFIX. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

