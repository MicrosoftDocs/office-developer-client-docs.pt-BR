---
title: Propriedade canônica PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 124a0d8f23fcff9d1bca9d5debe4a9aa6fb6146c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587114"
---
# <a name="pidlidremotetransport-canonical-property"></a>Propriedade canônica PidLidRemoteTransport

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identifica que conta o item de cabeçalho está associado, principalmente para implementar o deixe POP na funcionalidade do servidor. 
  
|||
|:-----|:-----|
|Propriedades associadas  <br/> |dispidRemoteXP  <br/> |
|Propriedade definida:  <br/> |PSETID_Remote  <br/> |
|ID de longo (LID):  <br/> |0x00008F03  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Mensagem remota  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é relevante somente em mensagens que têm uma classe de mensagem IPM. Remoto. Microsoft Outlook mantém um mapeamento de várias contas que estiver baixando os dados para um determinado repositório em uma mensagem de informações de associado de pasta (FAI), mas ele também pode manter essas informações no registro.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]] 
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

