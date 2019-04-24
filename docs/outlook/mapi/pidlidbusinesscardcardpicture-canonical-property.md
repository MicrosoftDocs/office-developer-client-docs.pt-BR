---
title: Propriedade canônica PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342004"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a>Propriedade canônica PidLidBusinessCardCardPicture

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a imagem a ser usada em um cartão de visita.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidBCCardPicture  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008041  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade deve ser um PNG (Portable Network Graphics) ou um fluxo JPEG. Essa propriedade deve ser usada em conjunto com a propriedade **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) da seguinte maneira: **dispidBCCardPicture** não deve estar presente em um contato se ** dispidBCDisplayDefinition** não está presente. Essa propriedade também não deve estar presente se os dados no **dispidBCCardPicture** não precisarem de uma imagem de cartão. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

