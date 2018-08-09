---
title: Responsabilidades do armazenamento de mensagens de texto formatado de suporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 301ebbf8e7a3e2a2deb303af5b198fd11511d495
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770518"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Suporte a texto formatado: responsabilidades do repositório de mensagens

  
  
**Aplica-se a**: Outlook 
  
Provedores de armazenamento de mensagem usam a propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para publicar se ou não podem lidar com Rich Text Format (RTF), texto HTML e, se ela sabe RTF, se eles armazenam o texto formatado em uma formato compactado ou descompactado. Provedores de armazenamento de mensagem indicam que eles estão cientes de RTF definindo o bit STORE_RTF_OK e que armazenam o texto formatado em um formulário descompactado definindo o bit STORE_UNCOMPRESSED_RTF. Provedores de armazenamento de mensagem indicam são reconhecem HTML definindo o bit STORE_HTML_OK.
  
Embora seja importante para um cliente de reconhecimento de RTF verificar se há o STORE_RTF_OK bit para determinar se ou não um armazenamento de mensagens suporta RTF, não é necessário para um cliente se preocupar com o formato de texto formatado de um repositório reconhecimento de RTF. 
  
Todos os repositórios de mensagem devem oferecer suporte a clientes sem reconhecimento de RTF. Um armazenamento de mensagens sem reconhecimento de RTF deve excluir a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) durante uma chamada para o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem se um cliente não tiver alterado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sem Atualizando **PR_RTF_IN_SYNC** ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Excluir **PR_RTF_IN_SYNC** faz com que a propriedade **PR_RTF_COMPRESSED** sejam recalculados da propriedade **PR_BODY** na próxima vez que um cliente RTF reconhecimento chama [RTFSync](rtfsync.md). 
  
A maioria dos repositórios de mensagem RTF reconhecimento não terá o texto da mensagem pelos clientes; ele deve ser computado na solicitação. Como esse cálculo é caro e demorado, os clientes devem usar **PR_RTF_COMPRESSED** sempre que possível. Para calcular a propriedade **PR_BODY** , o provedor de armazenamento de mensagem deve descompacte o conteúdo da propriedade **PR_RTF_COMPRESSED** e remover a formatação rich text. Os clientes que não têm suporte para a propriedade **PR_RTF_COMPRESSED** requerem esse cálculo ocorrer para cada mensagem. 
  
Ao copiar mensagens, a mensagem armazenar os provedores que não usam os métodos **IMAPISupport::DoCopyProps** ou **IMAPISupport::DoCopyTo** , correrá o risco de criação de uma mensagem com nenhum conteúdo se sua implementação exclui o **PR_BODY** propriedade e depende de **PR_RTF_COMPRESSED**. É possível para os dados na propriedade **PR_RTF_COMPRESSED** corrompido. Antes da exclusão de cada uma dessas propriedades de conteúdo da mensagem na operação de cópia, verifique corrupção da seguinte maneira: 
  
1. Se o valor da **PR_RTF_COMPRESSED** não for maior do que o RTF compactado, a propriedade está corrompida. 
    
2. Se o valor de mágica no cabeçalho RTF não for _dwMagicCompressedRTF_ ou _dwMagicUncompressedRTF_, a propriedade está corrompido.
    
Usando o suporte a métodos necessário não se preocupar com a implementação de uma verificação de corrupção **PR_RTF_COMPRESSED** ; de provedores de armazenamento de mensagem MAPI garante que as propriedades adequadas existirem e são válidas. 
  
Existem três níveis diferentes de suporte RTF que podem implementar provedores de armazenamento de mensagem; MAPI recomenda que o reconhecimento de RTF provedores de armazenamento de mensagem implementem seu suporte a nível intermediário ou mais alto. Todos os RTF reconhecimento mensagem repositório provedores cuidam da gerando **PR_BODY** a partir dos dados incluídos no **PR_RTF_COMPRESSED** nas mensagens de saída e fazer uma chamada para **RTFSync** para sincronizar o texto e a formatação em mensagens de entrada. 
  
As diferenças entre essas três níveis são descritas na tabela a seguir. 
  
|**Nível de suporte**|**Descrição**|
|:-----|:-----|
|Baixa  <br/> |Mensagem armazenar provedor chamadas **RTFSync** sempre que as alterações são salvas em uma mensagem e extrai os dados para a propriedade **PR_BODY** do **PR_RTF_COMPRESSED** em vez de exigir clientes para defini-la. **PR_BODY** e o **PR_RTF_COMPRESSED** são armazenados.  <br/> |
|Meio  <br/> |Mensagem armazenar provedor armazena apenas a propriedade **PR_RTF_COMPRESSED** , computação **PR_BODY** quando necessário.  <br/> |
|Alta  <br/> |Mensagem armazenar repositórios de provedor nem **PR_BODY** ou as propriedades RTF auxiliares. **RTFSync** é chamado quando o texto da mensagem foi alterada e a formatação permanecerá inalterada ou quando uma nova mensagem é baixada por um provedor de transporte.  <br/> |
   

