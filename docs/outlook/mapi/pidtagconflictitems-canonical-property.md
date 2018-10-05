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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386723"
---
# <a name="pidtagconflictitems-canonical-property"></a>Propriedade canônica PidTagConflictItems

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma ou mais IDs de itens que participaram de resolução de conflitos automática de entrada.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificador:  <br/> |0x1098  <br/> |
|Tipo de propriedade:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Comentários

Os tipos de itens padrão do Microsoft Outlook que oferecem suporte a resolução de conflito automática incluem os seguintes tipos de item padrão: itens de compromisso, itens de contato, itens de diário, itens de email, itens de reunião, itens de nota e itens de tarefa. Um item que pertence a uma classe de mensagem que derive de um desses tipos de item padrão também dá suporte a resolução de conflitos automática. No Microsoft Outlook 2003 e o Microsoft Office Outlook 2007, quando o Outlook sincroniza os itens e considera que existe uma possibilidade de que a cópia resultante não pode conter todos os dados essenciais, o Outlook armazena as cópias conflitantes nos **conflitos** pasta, sob a pasta **Problemas de sincronização** . 
  
> [!NOTE]
> **Problemas de sincronização** e suas subpastas estão ocultas até você clicar em **Lista de pastas** no menu **Ir** . 
  
Um item expõe a propriedade **PR_CONFLICT_ITEMS** se ele é um dos tipos de item que oferecem suporte a resolução de conflito automática, ganhou em uma resolução de conflito ou foi colocado na pasta **conflitos** devido a uma resolução de conflito. A pasta na qual o item é colocado determina o conteúdo de **PR_CONFLICT_ITEMS**. Se o item está localizado em alguma pasta que não seja a pasta **conflitos** e o item expõe a propriedade **PR_CONFLICT_ITEMS** , o item deve ter won a resolução de conflito e **PR_CONFLICT_ITEMS** conteria identificações de entrada de uma ou mais das os itens que perdidas na resolução de conflito. Se o item está localizado na pasta **conflitos** e o item expõe a propriedade **PR_CONFLICT_ITEMS** , esse item deve ter perdido a resolução de conflito e **PR_CONFLICT_ITEMS** conteria a identificação de entrada do item que won no conflito resolução. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Sobre as adições de MAPI](about-mapi-additions.md)
  
[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

