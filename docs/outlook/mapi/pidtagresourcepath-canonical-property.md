---
title: Propriedade canônica PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429856"
---
# <a name="pidtagresourcepath-canonical-property"></a>Propriedade canônica PidTagResourcePath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um caminho para o servidor do provedor de serviços.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Identificador:  <br/> |0x3E07  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O caminho contido nessas propriedades representa o caminho sugerido onde o usuário pode encontrar recursos. A definição dessas propriedades é específica do provedor. Por exemplo, um aplicativo de agendamento usa essas propriedades para especificar o local sugerido para seus arquivos de aplicativo de agendamento.
  
O perfil do usuário de mensagens fornece essas propriedades como uma conveniência para que um aplicativo cliente não tenha que solicitar ao usuário do sistema de mensagens um caminho de rede ou uma letra de unidade de rede.
  
O MAPI funciona apenas com nomes de arquivo no conjunto de caracteres do American National Standards Institute (ANSI). Os aplicativos que usam nomes de arquivo em um conjunto de caracteres do fabricante do equipamento original (OEM) devem convertê-los em ANSI antes de chamar o MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

