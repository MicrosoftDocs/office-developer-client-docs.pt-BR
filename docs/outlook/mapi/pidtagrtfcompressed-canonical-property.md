---
title: Propriedade canônica PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c93d850551e766e97292d5417c3be5577f557af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769874"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Propriedade canônica PidTagRtfCompressed

  
  
**Aplica-se a**: Outlook 
  
Contém a versão do formato Rich Text (RTF) do texto da mensagem, geralmente em formato compactado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Identificador:  <br/> |0x1009  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém o texto da mensagem mesmo que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mas em RTF. 
  
Texto da mensagem em RTF normalmente é armazenado em formato compactado. No entanto, alguns sistemas não compacte texto formatado. Para acomodá-los, MAPI fornece o valor de dwMagicUncompressedRTF para um cabeçalho de stream identificar RTF descompactado e o sinalizador **STORE_UNCOMPRESSED_RTF** no **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) da mensagem Armazene para indicar que ele pode armazenar descompactado RTF. 
  
Para obter o conteúdo desta propriedade, chame **OpenProperty**e chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md) com o sinalizador **MAPI_READ** . Para escrever para essa propriedade, abri-lo com os sinalizadores **MAPI_MODIFY** e **MAPI_CREATE** . Isso garante que os novos dados completamente substituam quaisquer dados antigos e que as gravações são realizadas usando o número mínimo de atualizações loja. 
  
Repositórios de mensagem que suportam RTF ignoram quaisquer alterações para o espaço em branco no texto da mensagem. Quando **PR_BODY** é armazenada pela primeira vez, o armazenamento de mensagens também gera e armazena essa propriedade. Se o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado subsequentemente e **PR_BODY** foi modificado, o armazenamento de mensagens chama a função [RTFSync](rtfsync.md) para assegurar a sincronização com a versão RTF. Se apenas o espaço em branco tiver sido alterado, as propriedades são deixadas inalteradas. Isso preserva qualquer RTF não trivial formatação quando a mensagem passa por clientes sem reconhecimento de RTF e sistemas de mensagens. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Codifica e decodifica stream compactado em corpos de mensagens RTF.
    
[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Encapsula formatos de conteúdo adicionais (por exemplo, HTML) na propriedade RTF corpo de mensagens e anexos.
    
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

