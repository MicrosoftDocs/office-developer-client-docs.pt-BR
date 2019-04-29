---
title: Suporte a responsabilidades de repositório de mensagens de texto formatado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 502ba82279664638c8e7e4ae68f74df74758918d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435513"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Suporte a texto formatado: responsabilidades do repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de repositórios de mensagens usam a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para publicar se eles podem ou não manipular o formato Rich Text (RTF), texto HTML e, se forem compatíveis com RTF, se armazenar o texto formatado em um formato compactado ou descompactado. Os provedores de repositórios de mensagens indicam que eles têm reconhecimento de RTF Configurando o bit STORE_RTF_OK e que armazenam o texto formatado em um formulário descompactado Configurando o bit STORE_UNCOMPRESSED_RTF. Os provedores de repositórios de mensagens indicam que são compatíveis com HTML definindo o bit STORE_HTML_OK.
  
Embora seja importante que um cliente de reconhecimento de RTF Verifique o bit de STORE_RTF_OK para determinar se um repositório de mensagens suporta RTF, não é necessário que um cliente esteja preocupado com o formato de um texto formatado de um repositório com reconhecimento de RTF. 
  
Todos os repositórios de mensagens devem oferecer suporte a clientes não cientes de RTF. Um repositório de mensagens que não reconhece RTF deve excluir a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) durante uma chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem se um cliente tiver alterado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sem Atualizando o **PR_RTF_IN_SYNC** ou o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). A exclusão de **PR_RTF_IN_SYNC** faz com que a propriedade **PR_RTF_COMPRESSED** seja recalculada a partir da propriedade **PR_BODY** na próxima vez que um cliente com reconhecimento de RTF chama [RTFSync](rtfsync.md). 
  
A maioria dos repositórios de mensagens com reconhecimento de RTF não recebe o texto da mensagem por clientes; Ele deve ser calculado sob solicitação. Como esse cálculo é de tempo demorado e caro, os clientes devem usar o **PR_RTF_COMPRESSED** sempre que possível. Para calcular a propriedade **PR_BODY** , o provedor do repositório de mensagens deve descompactar o conteúdo da propriedade **PR_RTF_COMPRESSED** e remover a formatação rich text. Os clientes que não oferecem suporte à propriedade **PR_RTF_COMPRESSED** exigem que esse cálculo ocorra para cada mensagem. 
  
Ao copiar mensagens, provedores de repositórios de mensagens que não usam o **IMAPISupport::D ocopyprops** ou **IMAPISupport:** os métodos de ocopyto do:D correm o risco de criar uma mensagem sem conteúdo se sua implementação exclui o **PR_BODY** Propriedade e se baseia no **PR_RTF_COMPRESSED**. É possível que os dados na propriedade **PR_RTF_COMPRESSED** estejam corrompidos. Antes de excluir qualquer uma dessas propriedades de conteúdo da mensagem na operação de cópia, verifique se há corrupção da seguinte maneira: 
  
1. Se o valor de **PR_RTF_COMPRESSED** não for maior do que o RTF compactado, a propriedade estará corrompida. 
    
2. Se o valor mágico no cabeçalho RTF não for _dwMagicCompressedRTF_ ou _dwMagicUncompressedRTF_, a propriedade estará corrompida.
    
Os provedores de repositórios de mensagens que usam os métodos de suporte não precisam se preocupar com a implementação de um cheque para corrupção do **PR_RTF_COMPRESSED** ; O MAPI garante que as propriedades apropriadas existam e sejam válidas. 
  
Há três níveis diferentes de suporte a RTF que os provedores de repositório de mensagens podem implementar; MAPI recomenda que os provedores de repositório de mensagens com reconhecimento de RTF implementem seu suporte no nível intermediário ou superior. Todos os provedores de repositório de mensagens compatíveis com RTF cuidam da geração de **PR_BODY** dos dados incluídos no **PR_RTF_COMPRESSED** nas mensagens de saída e fazem uma chamada para **RTFSync** para sincronizar texto e formatação em mensagens de entrada. 
  
As diferenças entre esses três níveis são descritas na tabela a seguir. 
  
|**Nível de suporte**|**Descrição**|
|:-----|:-----|
|Baixo  <br/> |O provedor de repositório de mensagens chama **RTFSync** sempre que as alterações são salvas em uma mensagem e extrai os dados para a propriedade **PR_BODY** do **PR_RTF_COMPRESSED** , em vez de exigir que os clientes o definam. Tanto **PR_BODY** quanto **PR_RTF_COMPRESSED** são armazenados.  <br/> |
|Middleware  <br/> |O provedor de repositório de mensagens armazena apenas a propriedade **PR_RTF_COMPRESSED** , calculando o **PR_BODY** quando necessário.  <br/> |
|Alto  <br/> |O provedor de repositório de mensagens não armazena **PR_BODY** ou as propriedades de RTF auxiliares. **RTFSync** é chamado quando o texto da mensagem foi alterado e a formatação permanece inalterada ou quando uma nova mensagem é baixada por um provedor de transporte.  <br/> |
   

