---
title: Propriedade canônica PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436822"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Propriedade canônica PidTagServiceDeleteFiles

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de nomes de FileNames que devem ser excluídos quando o serviço de mensagens é desinstalado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W  <br/> |
|Identificador:  <br/> |0x3D10  <br/> |
|Tipo de dados:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Os nomes de FileNames da lista contidos nessas propriedades são excluídos do computador ao usar o painel de controle para desinstalar o serviço de mensagens. Não inclua na lista qualquer DLL que ofereça suporte a vários serviços de mensagens ou que os serviços de mensagens adicionais possam ser removidos inadvertidamente.
  
O MAPI funciona somente com nomes de Filee outras cadeias de caracteres passadas para ele, no conjunto de caracteres ANSI. Os aplicativos que usam nomes de fileformados em um conjunto de caracteres OEM devem convertê-los para ANSI antes de chamar MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

