---
title: Propriedade canônica PidLidContactLinkSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319772"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>Propriedade canônica PidLidContactLinkSearchKey

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a lista de **SearchKeys** do contato vinculado a esse objeto de mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidContactLinkSearchKey  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008584  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

|**Comprimento em bytes**|**Descrição**|**Anotações**|
|:-----|:-----|:-----|
|2   <br/> |ContactEntryCount  <br/> |Nenhum  <br/> |
|variável  <br/> |Dados de SearchKey  <br/> |Repetir ContactEntryCount vezes  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também

- [Propriedades MAPI](mapi-properties.md) 
- [Propriedades canônicas MAPI](mapi-canonical-properties.md)
- [Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

