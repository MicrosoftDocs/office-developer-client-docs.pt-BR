---
title: Propriedade canônica PidTagConflictItems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338014"
---
# <a name="pidtagconflictitems-canonical-property"></a>Propriedade canônica PidTagConflictItems

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma ou mais IDs de entrada de itens envolvidos em uma resolução automática de conflitos.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificador:  <br/> |0x1098  <br/> |
|Tipo de propriedade:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Comentários

Os tipos de itens padrão do Microsoft Outlook que suportam a resolução automática de conflitos incluem os seguintes tipos de item padrão: itens de compromisso, itens de contato, itens de diário, itens de email, itens de reunião, itens de anotação sticky e itens de tarefa. Um item pertencente a uma classe de mensagem que deriva de um desses tipos de item padrão também oferece suporte à resolução automática de conflitos. No Microsoft Outlook 2003 e no Microsoft Office Outlook 2007, quando o Outlook sincroniza itens e considera que existe a possibilidade de  a cópia resultante  não conter todos os dados essenciais, o Outlook armazena as cópias conflitantes na pasta Conflitos, na pasta Problemas de Sincronização. 
  
> [!NOTE]
> **Problemas de** sincronização e suas subpastas ficam ocultos até que você clique em **Lista** de Pastas **no** menu Ir. 
  
Um item expõe a propriedade **PR_CONFLICT_ITEMS** se for um dos tipos de item que suportam resolução automática de  conflitos, tiver ganho em uma resolução de conflitos ou foi colocado na pasta Conflitos devido a uma resolução de conflitos. A pasta na qual o item é colocado determina o conteúdo PR_CONFLICT_ITEMS **.** Se o item estiver localizado em  alguma pasta diferente da pasta Conflitos e o item expor a propriedade **PR_CONFLICT_ITEMS,** o item deverá ter ganho a resolução de conflitos e **PR_CONFLICT_ITEMS** conterá uma ou mais IDs de entrada desses itens perdidos na resolução de conflitos. Se o item estiver  localizado na pasta Conflitos e o item expor a propriedade **PR_CONFLICT_ITEMS,** esse item deverá ter perdido PR_CONFLICT_ITEMS resolução de conflitos e PR_CONFLICT_ITEMS conteria **a** ID de entrada do item que ganhou na resolução de conflitos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Sobre as adições de MAPI](about-mapi-additions.md)
  
[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

