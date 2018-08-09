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
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769850"
---
# <a name="pidtagresourcepath-canonical-property"></a>Propriedade canônica PidTagResourcePath

  
  
**Aplica-se a**: Outlook 
  
Contém um caminho para o servidor do provedor de serviços.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Identificador:  <br/> |0x3E07  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O caminho contido nessas propriedades representa a sugestão de caminho onde o usuário pode localizar recursos. A definição dessas propriedades é específico do provedor. Por exemplo, um aplicativo de agendamento usa essas propriedades para especificar o local sugerido para seus arquivos de aplicativo de agendamento.
  
O perfil de usuário de mensagens fornece essas propriedades como conveniência para que um aplicativo cliente não precisa solicitar ao usuário de mensagens de um caminho de rede ou uma letra de unidade de rede.
  
MAPI funciona somente com nomes de arquivo no conjunto de caracteres American National Standards Institute (ANSI). Aplicativos que usam os nomes de arquivo em um conjunto de caracteres do fabricante do equipamento original (OEM) devem convertê-los para ANSI antes de chamar MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

