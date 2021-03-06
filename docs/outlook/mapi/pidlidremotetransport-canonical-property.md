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
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439440"
---
# <a name="pidlidremotetransport-canonical-property"></a>Propriedade canônica PidLidRemoteTransport

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identifica a qual conta o item de header está associado, principalmente para implementar a funcionalidade De saída POP no servidor. 
  
|||
|:-----|:-----|
|Propriedades Associadas  <br/> |dispidRemoteXP  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Remote  <br/> |
|Long ID (LID):  <br/> |0x00008F03  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Mensagem remota  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade só é relevante em mensagens que tenham uma classe de mensagem do IPM. Remoto. O Microsoft Outlook mantém um mapeamento de várias contas que estão baixando para um determinado armazenamento em uma mensagem FAI (Informações Associadas à Pasta), mas também pode manter essas informações no Registro.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]] 
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

