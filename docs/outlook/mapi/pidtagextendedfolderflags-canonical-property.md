---
title: Propriedade canônica PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382656"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Propriedade canônica PidTagExtendedFolderFlags
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os sinalizadores estendidos sobre uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Identificador:  <br/> |0x36DA  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é um fluxo binário que contém propriedades sub-recurso codificadas para a pasta. Ele é formatado como uma série de itens de sub de comprimento variável. Os primeiros 8 bits do item sub é um campo de ID, que indica que tipo de sinalizador o item de sub representa. Os segundo 8 bits é o número de bytes de dados que seguem.
  
Os valores de ID possíveis incluem:
  
- Inválido
    
   Não use esse valor
    
- ExtendedFlags
    
   Os dados são um valor de quatro bytes formatado como:
    
   |**Bits**|**Descrição**|
   |:-----|:-----|
   |0-1  <br/> |Reservado.  <br/> |
   |2  <br/> |Defina como 0 se o aplicativo deve mostrar uma descrição da política.  <br/> |
   |3 a 5  <br/> |Reservado.  <br/> |
   |6 e 7  <br/> |Controla a exibição do número de mensagens na pasta.  <br/> 0 - use a configuração padrão  <br/> 1 - use o número de mensagens não lidas  <br/> 3 - use o número total de mensagens  <br/> |
   |8-31  <br/> |Reservado.  <br/> |
   
Itens reservados podem ser ignorados, mas os valores existentes devem ser preservados.
    
- SearchFolderID
    
   O campo de dados é um campo de 16 bytes. Quando o aplicativo cria uma pasta de pesquisa persistente, defina esse campo na pasta para o mesmo valor que o **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) uma propriedade binária na mensagem de pasta de pesquisa.
    
- ToDoFolderVersion
    
   O campo de dados é um campo de 4 bytes. Quando o aplicativo cria a pasta de pesquisa de tarefas pendentes, ele deve definir o valor desse campo na pasta para o valor inteiro de pouca-endian da "0x000c0000":
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica o local e as propriedades de dados de configuração de cliente e servidor, como listas de categoria compartilhada e o horário de trabalho.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também

- [Propriedades MAPI](mapi-properties.md)
- [Propriedades MAPI canônicas](mapi-canonical-properties.md)
- [Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

