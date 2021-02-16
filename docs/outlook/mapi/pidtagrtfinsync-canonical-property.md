---
title: Propriedade canônica PidTagRtfInSync
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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357873"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Propriedade canônica PidTagRtfInSync

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se **a PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tem o mesmo conteúdo de texto que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para esta mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Identificador:  <br/> |0x0E1F  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Um valor TRUE significa que **a** propriedade PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)), a versão de texto sem formatação dessa mensagem e a propriedade PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a versão RTF (Rich Text Format), são idênticas, exceto para espaço em branco no **PR_BODY** e formatação em **PR_RTF_COMPRESSED**.  O texto nas duas versões consiste nos mesmos caracteres na mesma sequência.
  
Um valor FALSO significa que as duas versões não são sincronizadas para conteúdo de texto, mas são capazes de ser sincronizadas pela [função RTFSync.](rtfsync.md) Uma versão foi alterada e a outra não. 
  
Nenhum valor significa que as duas versões, se existirem ou nunca existirem, não poderão ser sincronizadas. Uma versão foi excluída ou alterada de forma radical para que a sincronização não seja mais possível.
  
Um aplicativo cliente que tenha modificado **PR_RTF_COMPRESSED** deve definir um valor FALSO nesta propriedade para forçar a sincronização. Os armazenamentos de mensagens com conhecimento RTF devem executar a sincronização usando **RTFSync** durante uma chamada [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Clientes com conhecimento de RTF devem verificar a configuração de **PR_RTF_IN_SYNC** antes de ler PR_RTF_COMPRESSED **e** chamar **RTFSync** primeiro, se necessário. 
  
Se **PR_BODY** tiver feito modificações em algo diferente de seu espaço em branco, o armazenamento de mensagens deverá **excluí-PR_RTF_IN_SYNC** para encerrar a sincronização. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
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

