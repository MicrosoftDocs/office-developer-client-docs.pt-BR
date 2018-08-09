---
title: Propriedade canônica PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770028"
---
# <a name="pidtagservicename-canonical-property"></a>Propriedade canônica PidTagServiceName

  
  
**Aplica-se a**: Outlook 
  
Contém o nome de um serviço de mensagem conforme definido pelo usuário no arquivo Mapisvc.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D09  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O nome contido nessas propriedades é específico para o serviço de mensagem. Ele proveniente da seção [serviços] em MAPISVC.
  
Essas propriedades aparecem como uma coluna na tabela de serviço de mensagem e podem ser usadas para filtrar os serviços. Porque ele é usado para identificar e filtrar os serviços, o valor não deve ser localizado.
  
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

