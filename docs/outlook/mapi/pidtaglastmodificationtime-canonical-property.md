---
title: Propriedade canônica PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279706"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Propriedade canônica PidTagLastModificationTime

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a data e a hora em que o objeto ou subobjeto foi modificado pela última vez. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Identificador:  <br/> |0x3008  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Hora da mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é inicialmente definida com o mesmo valor que a propriedade **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Os subobjetos de anexo podem atualizá-lo conforme necessário copiando o tempo da última modificação mantido pelo sistema de arquivos nativo. Um aplicativo cliente pode definir essa propriedade até a primeira chamada para o [método IMAPIProp::SaveChanges.](imapiprop-savechanges.md) A partir daí, o provedor deve atualizar **PR_LAST_MODIFICATION_TIME** durante cada chamada **IMAPIProp::SaveChanges.** 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
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

