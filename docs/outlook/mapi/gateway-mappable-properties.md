---
title: Propriedades mapeáveis do gateway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430473"
---
# <a name="gateway-mappable-properties"></a>Propriedades mapeáveis do gateway

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Propriedades de gateway mappable são propriedades que podem exigir tradução quando enviadas de um domínio de mensagens para outro. As propriedades mapeáveis de gateway de MAPI permitem que as mensagens incluam informações que exigem um gateway para garantir que o sistema de mensagens de destino as utilize corretamente. Embora os desenvolvedores de gateway não sejam obrigados a fornecer esse recurso de tradução, eles devem considerar as propriedades de gateway mappable como uma oportunidade para melhorar a manipulação do conteúdo da mensagem.
  
MAPI specifies five types of gateway-mappable properties:
  
- Nome diferenciado (DN)
    
- Nome para exibição
    
- Tipo de email
    
- Identificador de entrada
    
- Chave de pesquisa
    
Este é o conjunto de propriedades de endereçamento associadas a destinatários, senders, destinatários de relatório e destinatários e destinatários delegados. Para ajudar seu cliente a definir essas propriedades para que um gateway as manipulará especialmente, MAPI especifica uma convenção de nomenal usando propriedades nomeadas e conjuntos de propriedades. Existem cinco conjuntos de propriedades para manter propriedades nomeadas, as propriedades de endereçamento que exigem mapeamento. Há um conjunto de propriedades para cada tipo de propriedade mappable. Os conjuntos de propriedades que manterão essas propriedades de endereçamento nomeadas são os a seguir.
  
|**Conjunto de propriedades**|**Descrição**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contém propriedades de cadeia de caracteres usadas como nomes de exibição.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contém propriedades de cadeia de caracteres usadas como endereços de email.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contém propriedades de cadeia de caracteres usadas como tipos de endereço de email.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contém propriedades binárias usadas como identificadores de entrada de longo prazo.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contém propriedades binárias usadas como chaves de pesquisa.  <br/> |
   

