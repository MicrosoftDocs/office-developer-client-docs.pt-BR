---
title: Propriedade canônica PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331259"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a>Propriedade canônica PidLidSharingRemoteUid

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica a ID de entrada da pasta remota que está sendo compartilhada. Esta é uma propriedade de uma mensagem de compartilhamento.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSharingRemoteUid  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A06  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Compartilhamento  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade deve ser definida como a representação hexadecimal de cadeia de caracteres do valor da propriedade PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) na pasta que está sendo compartilhada. Esta é uma propriedade de uma mensagem de compartilhamento.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Compartilha pastas de caixa de correio entre clientes.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

