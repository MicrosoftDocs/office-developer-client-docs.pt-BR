---
title: Restrições de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 54cd90cac6c00e8cf274e0b78a1bfec32401bb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576509"
---
# <a name="address-book-restrictions"></a>Restrições de catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de catálogo de endereços são necessários para oferecer suporte a três tipos de restrições nos índices de conteúdo de seus contêineres:
  
- Restrições de propriedade de nome ambígua
    
- Restrições de propriedade de chave de instância
    
- Restrições de conteúdo de nome de exibição de prefixo
    
Restrições de nome ambígua são restrições de propriedade usando a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para corresponder os nomes dos destinatários com entradas nos contêineres de catálogo de endereços. A restrição de propriedade **PR_ANR** é um tipo de "melhor adivinhar" da pesquisa na qual provedores do catálogo de endereços podem escolher a propriedade correspondente que funciona melhor para seu contêiner. Por exemplo, um provedor de catálogo de endereços pode implementar a restrição **PR_ANR** por nomes de destinatário correspondentes contra a propriedade **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contêiner enquanto outro provedor pode usar **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI recomenda que implementações da restrição **PR_ANR** obter um equilíbrio entre desempenho adequado e satisfação do usuário. Satisfação do usuário pode ser comprometida quando um provedor de catálogo de endereços implementa a restrição de tal forma que forem encontradas correspondências poucos ou muitos. Suportam para alguns provedores de catálogo de endereços que é conhecido como um nome diferenciado ou comum que não é para exibição em uma caixa de diálogo, mas pode fazer a correspondência de uma restrição de nome ambígua. 
  
Uma implementação típica pode ser para analisar o nome para exibição do destinatário em palavras, a correspondência de qualquer entrada que contém todas as palavras. Atenção aos detalhes como a sensibilidade à posição do word, se as palavras não consecutivos são comparadas e a opção de caracteres separadores podem variar. Por exemplo, se o nome a ser resolvido for "Bill L", uma restrição de **PR_ANR** típica selecionaria as entradas a seguir como correspondência: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Jr do Logan. 
    
- Sam Bill Lee
    
Restrições de chave de instância ou restrições de propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), são usadas na implementação das caixas de listagem que são usados em aplicativos cliente para exibir as tabelas MAPI. Algumas implementações de caixa de lista permitem aos usuários fazer várias seleções, rolar para cima ou para baixo e retorno para o primeiro item selecionado. Para implementar esse comportamento, clientes [IMAPITable:: FindRow](imapitable-findrow.md), passando uma restrição de propriedade na propriedade **PR_INSTANCE_KEY** para o método de chamada. Provedores de catálogo de endereços são necessárias para dar suporte a essa restrição. 
  
Outro recurso das caixas de listagem usado para exibição de tabela é a capacidade para posicionar o cursor com base em um conjunto de caracteres de prefixo. À medida que o usuário começar a digitar caracteres de prefixo, o cliente move o cursor para o primeiro item começando com esses caracteres. Clientes implementam esse recurso com uma restrição de conteúdo com base na propriedade **PR_DISPLAY_NAME** e o nível de difusa FL_PREFIX. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

