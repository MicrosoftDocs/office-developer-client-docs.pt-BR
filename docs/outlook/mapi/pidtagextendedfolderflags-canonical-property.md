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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316349"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Propriedade canônica PidTagExtendedFolderFlags
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém sinalizadores estendidos sobre uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Identificador:  <br/> |0x36DA  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é um fluxo binário que contém sub-propriedades codificadas para a pasta. Ele é formatado como uma série de subsistros de comprimento variável. Os primeiros 8 bits do sub item é um campo de ID, que indica que tipo de sinalizador o sub item representa. O segundo 8 bits é o número de bytes de dados a seguir.
  
Os valores possíveis de ID incluem:
  
- Invalid
    
   Não use esse valor
    
- ExtendedFlags
    
   Os dados são um valor de quatro byte formatado como:
    
   |**Bits**|**Descrição**|
   |:-----|:-----|
   |0-1  <br/> |Reservado.  <br/> |
   |2   <br/> |De definida como 0 se o aplicativo deve mostrar uma descrição de política.  <br/> |
   |3-5  <br/> |Reservado.  <br/> |
   |6-7  <br/> |Controla a exibição do número de mensagens na pasta.  <br/> 0 - Usar a configuração padrão  <br/> 1 - Usar o número de mensagens não lidas  <br/> 3 - Usar o número total de mensagens  <br/> |
   |8-31  <br/> |Reservado.  <br/> |
   
Os itens reservados podem ser ignorados, mas os valores existentes devem ser preservados.
    
- SearchFolderID
    
   O campo de dados é um campo de 16 byte. Quando o aplicativo cria uma pasta de pesquisa persistente, ele deve definir esse campo na pasta com o mesmo valor que a propriedade binária **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) na Mensagem da Pasta de Pesquisa.
    
- ToDoFolderVersion
    
   O campo de dados é um campo de 4 byte. Quando o aplicativo cria a pasta de pesquisa de fazer, ele deve definir o valor desse campo na pasta como o valor inteiro little-endian de" 0x000c0000":
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica o local e as propriedades dos dados de configuração do cliente e do servidor, como listas de categorias compartilhadas e horas de trabalho.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também

- [Propriedades MAPI](mapi-properties.md)
- [Propriedades canônicas MAPI](mapi-canonical-properties.md)
- [Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

