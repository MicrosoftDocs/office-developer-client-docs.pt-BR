---
title: Propriedades podem ser mapeadas de gateway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 07c215511f010741e69c08c184df0ca3ce461e13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583614"
---
# <a name="gateway-mappable-properties"></a>Propriedades podem ser mapeadas de gateway

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Propriedades podem ser mapeados Gateway são propriedades que podem exigir a conversão quando enviada de um domínio de mensagens para outro. Propriedades podem ser mapeados gateway do MAPI habilitar as mensagens incluir informações que requer um gateway para garantir que o sistema de mensagens de destino utiliza adequadamente. Embora os desenvolvedores de gateway não são necessários para fornecer esse recurso de conversão, eles devem considerar propriedades podem ser mapeados gateway como uma oportunidade para aperfeiçoar o tratamento do conteúdo da mensagem.
  
MAPI Especifica cinco tipos de propriedades podem ser mapeados gateway:
  
- Nome para exibição
    
- Endereço de email
    
- Tipo de email
    
- Identificador de entrada
    
- Chave de pesquisa
    
Este é o conjunto de propriedades que estão associadas a destinatários, remetentes confiáveis, destinatários de relatório e delegados remetentes e destinatários de endereçamento. Para ajudar o seu cliente definir essas propriedades para que um gateway manipula especialmente, MAPI Especifica uma convenção de nomenclatura usando propriedades nomeadas e conjuntos de propriedades. Cinco conjuntos de propriedade existirem para armazenar propriedades nomeadas, as propriedades de endereçamento que exigem o mapeamento. Não há uma propriedade definida para cada tipo de propriedade podem ser mapeado. Os conjuntos de propriedades que irá manter essas propriedades endereçamento nomeadas são os seguintes.
  
|**Conjunto de propriedades**|**Descrição**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contém propriedades de cadeia de caracteres usadas como nomes de exibição.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contém propriedades de cadeia de caracteres usadas como endereços de email.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contém propriedades de cadeia de caracteres usadas como tipos de endereço de email.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contém propriedades binárias usadas como identificadores de entrada de longo prazo.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contém propriedades binárias usadas como chaves de pesquisa.  <br/> |
   

