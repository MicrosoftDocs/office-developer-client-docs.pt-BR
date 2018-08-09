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
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770092"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>Propriedade canônica PidTagStoreUnicodeMask

  
  
**Aplica-se a**: Outlook 
  
Contém uma bitmask dos sinalizadores que aplicativos cliente devem consultar para determinar as características de um armazenamento de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|Identificador:  <br/> |0x340F  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade revela as capacidades de um armazenamento de mensagens para aplicativos cliente do planejamento para enviá-la uma mensagem. Os sinalizadores podem facilitar decisões por um cliente ou outro repositório, como se deseja enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Um cliente nunca deve definir essa propriedade. Uma tentativa retorna **MAPI_E_COMPUTED**. 
  
Um ou mais dos seguintes sinalizadores podem ser definido para essa propriedade: 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) O armazenamento de mensagens oferece suporte a propriedades que contêm caracteres (8 bits), American National Standards Institute (ANSI).
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) O armazenamento de mensagens oferece suporte a vinculação e incorporação de objetos (OLE) ou não-OLE anexos de mensagens. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) O armazenamento de mensagens oferece suporte a categorizados modos de exibição das tabelas. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) O armazenamento de mensagens oferece suporte a criação de novas mensagens. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Identificadores de entrada para os objetos no repositório de mensagem são exclusivos, ou seja, nunca reutilizado durante a vida útil do repositório. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) O armazenamento de mensagens oferece suporte a mensagens HTML, armazenadas na propriedade **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Observe que **STORE_HTML_OK** não está definido em versões do MAPIDEFS. H que estão incluídos no Microsoft Exchange 2000 Server e versões anteriores. Se seu ambiente de desenvolvimento usa um MAPIDEFS. Arquivo de H que não incluem **STORE_HTML_OK**, use o valor da "0x00010000". 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Em um repositório PST encapsulado, indica que quando uma nova mensagem chega na loja, o repositório faz regras e spam filtrar processamento na mensagem separadamente. As repositório chamadas [IMAPISupport::Notify](imapisupport-notify.md), configuração **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e, em seguida, passa os detalhes da nova mensagem para o cliente de escutando. Subsequentemente, quando o cliente escutando recebe a notificação, ele não processar regras na mensagem. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Esse sinalizador é reservado e não deve ser usado.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) O armazenamento de mensagens oferece suporte a modificação das suas mensagens existentes. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) O armazenamento de mensagens oferece suporte a vários valores de propriedades, garante a estabilidade da ordem de valor em uma propriedade de valores múltiplos em toda uma gravação de operação e suporta instanciação das propriedades multivaloradas nas tabelas. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) O armazenamento de mensagens oferece suporte a notificações. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) O armazenamento de mensagens oferece suporte a anexos de OLE. Os dados OLE são acessíveis através de uma interface **IStorage** , tais como isto disponíveis por meio da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) As pastas nesse armazenamento são pública (multiusuário), não é particular (possivelmente várias instâncias, mas não multiusuário). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) O manipulador de protocolo MAPI não irá rastrear o repositório e o repositório é responsável por push quaisquer alterações por meio de notificações para o indexador para ter mensagens indexadas.
    
STORE_READONLY 
  
> (2, 0x00000002) Todas as interfaces para o armazenamento de mensagens têm um nível de acesso somente leitura. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) O armazenamento de mensagens oferece suporte a restrições. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) O armazenamento de mensagens oferece suporte a mensagens de formato Rich Text (RTF), geralmente compactadas, e o próprio repositório mantém **PR_BODY** e **PR_RTF_COMPRESSED** sincronizados. 
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) O armazenamento de mensagens oferece suporte a pastas de resultados de pesquisa. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) O armazenamento de mensagens oferece suporte a classificação de modos de exibição das tabelas. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) O armazenamento de mensagens oferece suporte a marcação de uma mensagem para envio. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) O armazenamento de mensagens suporta o armazenamento de mensagens de texto (RTF) do formulário revisable descompactado. Um fluxo RTF descompactado é identificado pelo valor **dwMagicUncompressedRTF** no cabeçalho stream. O valor de **dwMagicUncompressedRTF** é definido no RTFLIB. Arquivo H. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) O armazenamento de mensagens oferece suporte a propriedades que contém caracteres Unicode.
    
Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o armazenamento de mensagens é sem reconhecimento de RTF. Se o bit STORE_RTF_OK não estiver definido para um determinado repositório, um cliente de manutenção de versões RTF deve próprio chamar a função [RTFSync](rtfsync.md) para manter as versões de **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para conteúdo de texto. RTF sempre será armazenado em **PR_RTF_COMPRESSED**, se ele é realmente compactado ou não. 
  
## <a name="related-resources"></a>Recursos relacionados

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

