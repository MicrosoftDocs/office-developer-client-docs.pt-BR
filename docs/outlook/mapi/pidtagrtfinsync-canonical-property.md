---
title: Propriedade canônico de PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769885"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Propriedade canônico de PidTagRtfInSync

  
  
**Aplica-se a**: Outlook 
  
Conterá TRUE se a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tem o mesmo conteúdo de texto que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para esta mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Identificador:  <br/> |0x0E1F  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Coment�rios

Um valor de verdadeiro significa que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a versão de texto sem formatação dessa mensagem e a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a versão do formato Rich Text (RTF), são idênticas, exceto para espaço em branco no **PR_BODY** e a formatação **PR_RTF_COMPRESSED**. O texto nas duas versões consiste nos mesmos caracteres na mesma sequência.
  
Um valor FALSE significa que as duas versões não estão sincronizadas para conteúdo de texto, mas são capazes de sendo sincronizados pela função [RTFSync](rtfsync.md) . Uma versão tenha sido alterada, e a outra versão não tem. 
  
Nenhum valor significa que as duas versões, se ambos existirem ou existiam alguma, não podem ser sincronizadas. Uma versão foi excluída ou alterada radicalmente que sincronização não é mais possível.
  
Um aplicativo cliente que tenha modificado **PR_RTF_COMPRESSED** deve definir um valor False nessa propriedade para forçar a sincronização. Repositórios de mensagem RTF reconhecimento devem realizar a sincronização usando **RTFSync** durante uma chamada de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Clientes de reconhecimento de RTF devem verificar a configuração de **PR_RTF_IN_SYNC** antes de ler **PR_RTF_COMPRESSED**e chamar **RTFSync** primeiro, se necessário. 
  
Se **PR_BODY** teve modificações como algo diferente de seus espaços em branco, o armazenamento de mensagens deve excluir **PR_RTF_IN_SYNC** para encerrar a sincronização. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

