---
title: Propriedade canônica PidTagStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8d9f6311b19ddb489885004a9e507f780d9f1ea9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770089"
---
# <a name="pidtagstoresupportmask-canonical-property"></a>Propriedade canônica PidTagStoreSupportMask

  
  
**Aplica-se a**: Outlook 
  
Contém uma bitmask dos sinalizadores nessa consulta de aplicativos de cliente para determinar as características de um armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_SUPPORT_MASK  <br/> |
|Identificador:  <br/> |0x340D  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade revela as capacidades de um armazenamento de mensagens para aplicativos cliente que estiver planejando para enviá-la uma mensagem. Os sinalizadores podem oferecer suporte a decisões por um cliente ou outro repositório, como se deseja enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Um cliente nunca deve definir **PR_STORE_SUPPORT_MASK**; uma tentativa de definir este sinalizador retorna MAPI_E_COMPUTED. 
  
Um ou mais dos seguintes sinalizadores podem ser definidas para o bitmask **PR_STORE_SUPPORT_MASK** : 
  
STORE_ANSI_OK
  
> (131072, 0x00020000) O armazenamento de mensagens oferece suporte a propriedades que contêm caracteres do ANSI (8 bits).
    
STORE_ATTACH_OK 
  
> (32, 0x00000020) O armazenamento de mensagens oferece suporte a anexos (OLE ou não-OLE) às mensagens. 
    
STORE_CATEGORIZE_OK 
  
> (1024, 0x00000400) O armazenamento de mensagens oferece suporte a categorizados modos de exibição das tabelas. 
    
STORE_CREATE_OK 
  
> (16, 0x00000010) O armazenamento de mensagens oferece suporte a criação de novas mensagens. 
    
STORE_ENTRYID_UNIQUE 
  
> (1, 0x00000001) Identificadores de entrada para os objetos no repositório de mensagem são exclusivos, ou seja, nunca reutilizado durante a vida útil do repositório. 
    
STORE_HTML_OK 
  
> (65536, 0x00010000) O armazenamento de mensagens oferece suporte a mensagens HTML, armazenadas na propriedade **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)). Se seu ambiente de desenvolvimento usa um MAPIDEFS. Arquivo H que não inclui STORE_HTML_OK, use o valor 0x00010000 em vez disso. 
    
STORE_ITEMPROC
  
> (2097152, 0x00200000) Em um repositório PST encapsulado, indica que, quando uma nova mensagem chega na loja, o repositório executa regras e filtro de spam de processamento na mensagem separadamente. As repositório chamadas [IMAPISupport::Notify](imapisupport-notify.md), configuração **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e, em seguida, passa os detalhes da nova mensagem para o cliente de escutando. Subsequentemente, quando o cliente escutando recebe a notificação, ele não processar regras na mensagem. 
    
STORE_LOCALSTORE
  
> (524288, 0x00080000) Esse sinalizador é reservado e não deve ser usado.
    
STORE_MODIFY_OK 
  
> (8, 0x00000008) O armazenamento de mensagens oferece suporte a modificação das suas mensagens existentes. 
    
STORE_MV_PROPS_OK 
  
> (512, 0x00000200) O armazenamento de mensagens oferece suporte a vários valores de propriedades, garante a estabilidade da ordem de valor em uma propriedade de valores múltiplos em toda uma gravação de operação e suporta instanciação das propriedades multivaloradas nas tabelas. 
    
STORE_NOTIFY_OK 
  
> (256, 0x00000100) O armazenamento de mensagens oferece suporte a notificações. 
    
STORE_OLE_OK 
  
> (64, 0x00000040) O armazenamento de mensagens oferece suporte a anexos de OLE. Os dados OLE podem ser acessados através de uma interface **IStorage** , como disponível por meio da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). 
    
STORE_PUBLIC_FOLDERS 
  
> (16384, 0x00004000) As pastas nesse armazenamento são pública (multiusuário), não é particular (possivelmente várias instâncias, mas não multiusuário). 
    
STORE_PUSHER_OK
  
> (8388608, 0x00800000) O manipulador de protocolo MAPI não irá rastrear o repositório e o repositório é responsável para envio quaisquer alterações por meio de notificações por push para o indexador para ter mensagens indexadas.
    
STORE_READONLY 
  
> (2, 0x00000002) Todas as interfaces para o armazenamento de mensagens têm um nível de acesso somente leitura. 
    
STORE_RESTRICTION_OK 
  
> (4096, 0x00001000) O armazenamento de mensagens oferece suporte a restrições. 
    
STORE_RTF_OK 
  
> (2048, 0x00000800) O armazenamento de mensagens oferece suporte a mensagens de formato Rich Text (RTF), geralmente compactadas, e o próprio repositório mantém **PR_BODY** e **PR_RTF_COMPRESSED** sincronizados. 
    
STORE_RULES_OK
  
> (268435456, 0x10000000) Indica que as regras devem ser armazenadas nesse repositório PST, mesmo se ele não é o repositório padrão. Quando **STORE_RULES_OK** é usado em conjunto com **NON_EMS_XP_SAVE**, as regras são poderão ser executadas em repositórios de PST quebrado automaticamente não-padrão.
    
STORE_SEARCH_OK 
  
> (4, 0x00000004) O armazenamento de mensagens oferece suporte a pastas de resultados de pesquisa. 
    
STORE_SORT_OK 
  
> (8192, 0x00002000) O armazenamento de mensagens oferece suporte a classificação de modos de exibição das tabelas. 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080) O armazenamento de mensagens oferece suporte a marcação de uma mensagem para envio. 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768, 0x00008000) O armazenamento de mensagens suporta o armazenamento de mensagens RTF no formato descompactado. Um fluxo RTF descompactado é identificado pelo valor **dwMagicUncompressedRTF** no cabeçalho stream. O valor de **dwMagicUncompressedRTF** é definido no RTFLIB. Arquivo H. 
    
STORE_UNICODE_OK
  
> (262144, 0x00040000) Indica que o armazenamento de mensagens oferece suporte a Unicode armazenamento. Um cliente pode consultar a presença do sinalizador para decidir se deseja solicitar ou salvar a informação de Unicode para o repositório. 
    
Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o armazenamento de mensagens é sem reconhecimento de RTF. Se o bit STORE_RTF_OK não estiver definido para um determinado repositório, um cliente de manutenção de versões RTF deve próprio chamar a função [RTFSync](rtfsync.md) para manter as versões de **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para conteúdo de texto. RTF sempre será armazenado em **PR_RTF_COMPRESSED**, se ele é realmente compactado ou não. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)
  
> Descreve o formato das mensagens usado para enviar informações relacionadas ao compartilhamento de pastas no cliente.
    
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

