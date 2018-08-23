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
ms.openlocfilehash: 1c2089eee731fea8c80d8811f6b2e9f3c75ad1cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570524"
---
# <a name="pidtaggender-canonical-property"></a>Propriedade canônica PidTagGender

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o gênero do usuário mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_GENDER  <br/> |
|Identificador:  <br/> |0x3A4D  <br/> |
|Tipo de dados:  <br/> |PT_I2  <br/> |
|Área:  <br/> |Usuário de email MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade oferece acesso a informações sobre um usuário de mensagens e identificação e o conteúdo é. O conteúdo é definido pelo usuário mensagens e organização de mensagens do usuário. 
  
Os valores possíveis para essa propriedade são definidos na enumeração gênero. Eles estão listados da seguinte maneira:
  
|**Enumeração gênero**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |Gênero do contato não for especificado.  <br/> |
|genderFemale  <br/> |0x0001  <br/> |O contato está feminino.  <br/> |
|genderMale  <br/> |0x0002  <br/> |O contato está Masculino.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
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

