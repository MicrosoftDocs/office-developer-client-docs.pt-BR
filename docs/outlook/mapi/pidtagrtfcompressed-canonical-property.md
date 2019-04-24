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
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357887"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Propriedade canônica PidTagRtfCompressed

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a versão do formato Rich Text (RTF) do texto da mensagem, geralmente em formato compactado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Identificador:  <br/> |0x1009  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém o mesmo texto de mensagem que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mas em RTF. 
  
Normalmente, o texto da mensagem em RTF é armazenado em formato compactado. No enTanto, alguns sistemas não compactam o texto formatado. Para acomodá-los, o MAPI fornece o valor dwMagicUncompressedRTF para um cabeçalho de fluxo para identificar o RTF descompactado e o sinalizador **STORE_UNCOMPRESSED_RTF** no **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para a mensagem Store para indicar que pode armazenar RTF não compactado. 
  
Para obter o conteúdo dessa propriedade, chame **OpenProperty**e, em seguida, chame [WrapCompressedRTFStream](wrapcompressedrtfstream.md) com o sinalizador **MAPI_READ** . Para gravar nessa propriedade, abra-a com os sinalizadores **MAPI_MODIFY** e **MAPI_CREATE** . Isso garante que os novos dados substituam completamente quaisquer dados antigos e que as gravações sejam realizadas usando o número mínimo de atualizações de armazenamento. 
  
Os repositórios de mensagens que oferecem suporte a RTF ignoram qualquer alteração no espaço em branco no texto da mensagem. Quando o **PR_BODY** é armazenado pela primeira vez, o repositório de mensagens também gera e armazena essa propriedade. Se o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) for subsequentemente chamado e **PR_BODY** tiver sido modificado, o repositório de mensagens chamará a função [RTFSync](rtfsync.md) para garantir a sincronização com a versão RTF. Se apenas o espaço em branco tiver sido alterado, as propriedades permanecerão inalteradas. Isso preserva qualquer formatação RTF não trivial quando a mensagem viaja por clientes e sistemas de mensagens que não reconhecem RTF. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Codifica e decodifica um fluxo compactado em corpos de mensagens RTF.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Encapsula formatos de conteúdo adicionais (como HTML) dentro da propriedade de corpo RTF de mensagens e anexos.
    
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

