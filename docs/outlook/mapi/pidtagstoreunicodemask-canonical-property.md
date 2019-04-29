---
title: Propriedade canônica PidTagStoreUnicodeMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437935"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>Propriedade canônica PidTagStoreUnicodeMask

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de sinalizadores que os aplicativos clientes devem consultar para determinar as características de um repositório de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Identificador:  <br/> |0x340F  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Repositório de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade divulga os recursos de um repositório de mensagens para os aplicativos cliente que planejam enviar uma mensagem. Os sinalizadores podem facilitar as decisões de um cliente ou de outra loja, como se enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Um cliente nunca deve definir essa propriedade. Uma tentativa retorna **MAPI_E_COMPUTED**. 
  
Um ou mais dos seguintes sinalizadores podem ser definidos para esta propriedade: 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) O repositório de mensagens oferece suporte a propriedades que contenham caracteres ANSI (8 bits) da América do Instituto Nacional.
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) O repositório de mensagens oferece suporte a anexos de vinculação e incorporação de objetos (OLE) ou não OLE a mensagens. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) O repositório de mensagens oferece suporte a exibições categorizadas de tabelas. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) O repositório de mensagens oferece suporte à criação de novas mensagens. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Os identificadores de entrada para os objetos no repositório de mensagens são exclusivos, ou seja, nunca reutilizados durante a vida da loja. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) O repositório de mensagens oferece suporte a mensagens HTML, armazenadas na propriedade **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Observe que **STORE_HTML_OK** não está definido nas versões do MAPIDEFS. O H que está incluído no Microsoft Exchange 2000 Server e versões anteriores. Se seu ambiente de desenvolvimento usa um MAPIDEFS. H que não inclui o **STORE_HTML_OK**, use o valor "0x00010000" em vez disso. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Em um repositório PST encapsulado, indica que quando uma nova mensagem chega na loja, o repositório é regras e processamento de filtro de spam na mensagem separadamente. O repositório chama [IMAPISupport:: Notify](imapisupport-notify.md), setting **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e, em seguida, passa os detalhes da nova mensagem para o cliente de escuta. Posteriormente, quando o cliente de escutará recebe a notificação, ele não processará regras na mensagem. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Este sinalizador é reservado e não deve ser usado.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) O repositório de mensagens oferece suporte à modificação de suas mensagens existentes. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) O repositório de mensagens oferece suporte a propriedades com vários valores, garante a estabilidade da ordem de valor em uma propriedade de vários valores durante uma operação de salvamento e oferece suporte à instanciação de propriedades com vários valores em tabelas. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) O repositório de mensagens oferece suporte a notificações. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) O repositório de mensagens oferece suporte a anexos OLE. Os dados OLE podem ser acessados por meio de uma interface **IStorage** , como o disponível através da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) As pastas neste repositório são públicas (multiusuário), não privadas (possivelmente com várias instâncias, mas não vários usuários). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) O manipulador de protocolo MAPI não rastreará o repositório e o repositório será responsável por enviar todas as alterações por meio de notificações para o indexador para ter mensagens indexadas.
    
STORE_READONLY 
  
> (2, 0x00000002) Todas as interfaces para o repositório de mensagens têm um nível de acesso somente leitura. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) O repositório de mensagens oferece suporte a restrições. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) O repositório de mensagens oferece suporte a mensagens no formato Rich Text (RTF), geralmente compactadas, e a loja em si mantém o **PR_BODY** e o **PR_RTF_COMPRESSED** sincronizados. 
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) O repositório de mensagens oferece suporte a pastas de resultados de pesquisa. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) O repositório de mensagens oferece suporte à classificação de exibições de tabelas. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) O repositório de mensagens oferece suporte à marcação de uma mensagem para envio. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) O repositório de mensagens oferece suporte ao armazenamento de mensagens de texto de formulário revisadas (RTF) em formato descompactado. Um fluxo RTF descompactado é identificado pelo valor **dwMagicUncompressedRTF** no cabeçalho Stream. O valor **dwMagicUncompressedRTF** é definido em RTFLIB. Arquivo H. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) O repositório de mensagens oferece suporte a propriedades que contêm caracteres Unicode.
    
Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o repositório de mensagens não reconhece RTF. Se o bit STORE_RTF_OK não for definido para um repositório específico, um cliente que mantém as versões RTF deve chamar a função [RTFSync](rtfsync.md) para manter as versões **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para o conteúdo de texto. O RTF sempre é armazenado no **PR_RTF_COMPRESSED**, independentemente de ser compactado ou não. 
  
## <a name="related-resources"></a>Recursos relacionados

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

