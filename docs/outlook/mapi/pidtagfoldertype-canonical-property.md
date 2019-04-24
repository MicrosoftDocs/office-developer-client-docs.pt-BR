---
title: Propriedade canônica PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316314"
---
# <a name="pidtagfoldertype-canonical-property"></a>Propriedade canônica PidTagFolderType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma constante que indica o tipo de pasta. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FOLDER_TYPE  <br/> |
|Identificador:  <br/> |0x3601  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores:
  
FOLDER_GENERIC 
  
> Uma pasta genérica que contém mensagens e outras pastas.
    
FOLDER_ROOT 
  
> A pasta raiz da tabela de hierarquia de pastas, ou seja, uma pasta que não tem uma pasta pai.
    
FOLDER_SEARCH 
  
> Uma pasta que contém os resultados de uma pesquisa, na forma de links para mensagens que atendem aos critérios de pesquisa.
    
A raiz de um repositório de mensagens não deve ser confundida com a raiz da sub-árvore da mensagem interpessoal (IPM) nesse repositório. A pasta raiz do repositório, que não tem um pai, é obtida chamando o método [IMsgStore:: OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo. A pasta raiz da sub-árvore IPM, que tem um pai, é obtida usando o valor da propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) para a chamada **OpenEntry** . 
  
MAPI permite apenas uma pasta raiz por repositório de mensagens. Esta pasta contém mensagens e outras pastas. A propriedade **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) da pasta raiz contém o próprio identificador de entrada da pasta.
  
As informações em uma pasta de resultados de pesquisa são principalmente armazenadas na tabela de conteúdo, que contém as mesmas colunas de uma tabela de conteúdo típica, bem como duas colunas extras que identificam a pasta na qual cada mensagem foi encontrada: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (nome para exibição, obrigatório) e essa propriedade (identificador de entrada, opcional).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla as operações da pasta.
    
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

