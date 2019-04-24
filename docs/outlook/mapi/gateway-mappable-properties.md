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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320997"
---
# <a name="gateway-mappable-properties"></a>Propriedades mapeáveis do gateway

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Propriedades mapeadas pelo gateway são propriedades que podem exigir tradução quando enviadas de um domínio de mensagens para outro. As propriedades mapeadas pelo gateway MAPI permitem que as mensagens incluam informações que exijam um gateway para garantir que o sistema de mensagens de destino o use adequadamente. Embora os desenvolvedores de gateway não precisem fornecer esse recurso de conversão, eles devem considerar as propriedades de mapeáveis de gateway como uma oportunidade de melhorar o tratamento do conteúdo da mensagem.
  
MAPI especifica cinco tipos de propriedades do gateway-mapeáveis:
  
- Nome diferenciado (DN)
    
- Nome para exibição
    
- Tipo de email
    
- Identificador de entrada
    
- Chave de pesquisa
    
Este é o conjunto de propriedades de endereçamento que estão associadas a destinatários, remetentes, destinatários de relatórios e remetentes e destinatários delegados. Para ajudar seu cliente a definir essas propriedades para que um gateway as manipule especialmente, MAPI especifica uma Convenção de nomenclatura usando propriedades nomeadas e conjuntos de propriedades. Cinco conjuntos de propriedades existem para reter propriedades nomeadas, as propriedades de endereçamento que exigem mapeamento. Há um conjunto de propriedades para cada tipo de propriedade mapeável. Os conjuntos de propriedades que armazenarão essas propriedades de endereçamento nomeadas são os seguintes:
  
|**Conjunto de propriedades**|**Descrição**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contém propriedades de cadeia de caracteres usadas como nomes de exibição.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contém propriedades de cadeia de caracteres usadas como endereços de email.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contém propriedades de cadeia de caracteres usadas como tipos de endereço de email.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contém propriedades binárias usadas como identificadores de entrada de longo prazo.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contém propriedades binárias usadas como chaves de pesquisa.  <br/> |
   

