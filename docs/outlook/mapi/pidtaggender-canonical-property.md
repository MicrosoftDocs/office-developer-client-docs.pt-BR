---
title: Propriedade canônica PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316153"
---
# <a name="pidtaggender-canonical-property"></a>Propriedade canônica PidTagGender

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o sexo do usuário de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_GENDER  <br/> |
|Identificador:  <br/> |0x3A4D  <br/> |
|Tipo de dados:  <br/> |PT_I2  <br/> |
|Área:  <br/> |Usuário de email MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade fornece informações de identificação e acesso sobre um usuário de mensagens e o conteúdo é. O conteúdo é definido pelo usuário de mensagens e pela organização do usuário de mensagens. 
  
Os valores possíveis para essa propriedade são definidos na enumeração sexo. Eles estão listados da seguinte maneira:
  
|**Enumeração sexo**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |O sexo do contato não está especificado.  <br/> |
|genderFemale  <br/> |0x0001  <br/> |O contato é fêmea.  <br/> |
|genderMale  <br/> |0x0002  <br/> |O contato é macho.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.
    
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

