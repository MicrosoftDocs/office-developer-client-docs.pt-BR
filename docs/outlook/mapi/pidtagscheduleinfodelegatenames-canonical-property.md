---
title: Propriedade canônica PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 06462f992ec640992b95b89a618e7d82290eeeef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574500"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a>Propriedade canônica PidTagScheduleInfoDelegateNames

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os nomes dos representantes.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W  <br/> |
|Identificador:  <br/> |0x6844  <br/> |
|Tipo de dados:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Informações de disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Cada entrada nessas propriedades deve conter o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do catálogo de endereços do cada representante.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.
    
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

