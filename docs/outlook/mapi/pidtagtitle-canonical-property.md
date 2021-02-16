---
title: Propriedade canônica PidTagTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTitle
api_type:
- COM
ms.assetid: f35bbcc3-15dd-40ab-9bf4-bdb21f95d464
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2501ea7c4be08b0bec3c2d65e6a504df47dfc488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358762"
---
# <a name="pidtagtitle-canonical-property"></a>Propriedade canônica PidTagTitle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o cargo do destinatário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_TITLE, PR_TITLE_A, PR_TITLE_W  <br/> |
|Identificador:  <br/> |0x3A17  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Usuário de email MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades fornecem informações de identificação e acesso para um destinatário. Eles são definidos pelo destinatário e pela organização do destinatário. 
  
Essas propriedades são comumente usadas para indicar o cargo formal do destinatário, como Programador Sênior, em vez de uma classe completa, como programador. Normalmente, ele não é usado para títulos de "sufixo", como Esq. ou DDS.
  
Os valores comuns para essa propriedade incluem: Managing Director, Programmer II, Associate Professor e Development Lead. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.
    
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

