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
  
Contém uma máscara de bits de sinalizadores que os aplicativos cliente devem consultar para determinar as características de um armazenamento de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Identificador:  <br/> |0x340F  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade divulga os recursos de um armazenamento de mensagens para aplicativos cliente que planejam enviar uma mensagem a ele. Os sinalizadores podem facilitar as decisões por um cliente ou outro armazenamento, como se você deve enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Um cliente nunca deve definir essa propriedade. Uma tentativa retorna **MAPI_E_COMPUTED**. 
  
Um ou mais dos sinalizadores a seguir podem ser definidos para essa propriedade: 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) O armazenamento de mensagens oferece suporte a propriedades que contêm caracteres anSI (American National Standards Institute) (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) O armazenamento de mensagens dá suporte a OLE (Vinculação e Incorporação de Objetos) ou anexos não OLE a mensagens. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) O armazenamento de mensagens dá suporte a exibições categorizadas de tabelas. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) O armazenamento de mensagens oferece suporte à criação de novas mensagens. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Os identificadores de entrada para os objetos no armazenamento de mensagens são exclusivos, ou seja, nunca reutilizáveis durante a vida útil do armazenamento. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) O armazenamento de mensagens dá suporte a mensagens HTML, armazenadas **na PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Observe que **STORE_HTML_OK** não está definido em versões de MAPIDEFS. H que estão incluídos no Microsoft Exchange 2000 Server e versões anteriores. Se seu ambiente de desenvolvimento usa um MAPIDEFS. Arquivo H que não **inclui** STORE_HTML_OK , use o valor "0x00010000". 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Em um armazenamento PST empacotado, indica que, quando uma nova mensagem chega ao armazenamento, o armazenamento faz o processamento de regras e filtros de spam na mensagem separadamente. O armazenamento chama [IMAPISupport::Notify](imapisupport-notify.md), definindo **fnevNewMail** na estrutura [NOTIFICATION](notification.md) que é passada como um parâmetro e passa os detalhes da nova mensagem para o cliente de escuta. Posteriormente, quando o cliente de escutará recebe a notificação, ele não processará regras na mensagem. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Esse sinalizador é reservado e não deve ser usado.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) O armazenamento de mensagens dá suporte à modificação de suas mensagens existentes. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) O armazenamento de mensagens oferece suporte a propriedades de múltiplos valores, garante a estabilidade da ordem de valor em uma propriedade de múltiplos valores ao longo de uma operação de salvar e oferece suporte à instaciação de propriedades de múltiplos valores em tabelas. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) O armazenamento de mensagens oferece suporte a notificações. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) O armazenamento de mensagens dá suporte a anexos OLE. Os dados OLE podem ser acessados por meio de uma interface **IStorage,** como os disponíveis por meio da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) As pastas nesse armazenamento são públicas (multiusuárias), não privadas (possivelmente com várias instâncias, mas não com vários usuários). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) O Manipulador de Protocolo MAPI não rastreará o armazenamento, e o armazenamento é responsável por enviar quaisquer alterações por meio de notificações ao indexador para que as mensagens tenham sido indexadas.
    
STORE_READONLY 
  
> (2, 0x00000002) Todas as interfaces para o armazenamento de mensagens têm um nível de acesso somente leitura. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) O armazenamento de mensagens oferece suporte a restrições. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) O armazenamento de mensagens dá suporte a mensagens RTF (Rich Text Format), geralmente compactadas, e o próprio armazenamento mantém PR_BODY **e** **PR_RTF_COMPRESSED** sincronizados. 
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) O armazenamento de mensagens oferece suporte a pastas de resultados de pesquisa. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) O armazenamento de mensagens oferece suporte à classificação de exibições de tabelas. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) O armazenamento de mensagens dá suporte à marcação de uma mensagem para envio. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) O armazenamento de mensagens oferece suporte ao armazenamento de mensagens de texto de formulário revisível (RTF) em formato não compactado. Um fluxo RTF não compactado é identificado pelo valor **dwMagicUncompressedRTF** no header de fluxo. O **valor dwMagicUncompressedRTF** é definido no RTFLIB. Arquivo H. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) O armazenamento de mensagens dá suporte a propriedades que contêm caracteres Unicode.
    
Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o armazenamento de mensagens não reconhece RTF. Se o bit STORE_RTF_OK não estiver definido para um determinado armazenamento, um cliente que mantém versões RTF deverá chamar a função [RTFSync](rtfsync.md) para manter as versões **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para conteúdo de texto. O RTF é sempre armazenado **PR_RTF_COMPRESSED**, seja realmente compactado ou não. 
  
## <a name="related-resources"></a>Recursos relacionados

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

