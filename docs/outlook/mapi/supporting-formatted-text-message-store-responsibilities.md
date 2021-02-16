---
title: Suporte às responsabilidades do armazenamento de mensagens de texto formatado
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
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Suporte a texto formatado: responsabilidades do armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de repositório de mensagens usam a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para publicar se podem ou não manipular RTF (Rich Text Format), texto HTML e, se são cientes de RTF, se armazenam o texto formatado em um formato compactado ou descompactado. Os provedores de armazenamento de mensagens indicam que estão cientes de RTF definindo o bit STORE_RTF_OK e que armazenam o texto formatado em um formulário descompactado definindo o STORE_UNCOMPRESSED_RTF bit. Os provedores de armazenamento de mensagens indicam que estão cientes de HTML definindo o STORE_HTML_OK bit.
  
Embora seja importante que um cliente com conhecimento de RTF verifique o bit STORE_RTF_OK para determinar se um armazenamento de mensagens dá suporte ou não a RTF, não é necessário que um cliente se preocupe com o formato do texto formatado de um armazenamento com conhecimento RTF. 
  
Todos os armazenamentos de mensagens devem dar suporte a clientes que não reconhecem RTF. Um armazenamento de mensagens que não reconhece RTF deve excluir a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) durante uma chamada para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem se um cliente tiver alterado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sem atualizar PR_RTF_IN_SYNC **ou** **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). A **exclusão PR_RTF_IN_SYNC** faz com que a **propriedade PR_RTF_COMPRESSED** seja recomputada da propriedade **PR_BODY** na próxima vez que um cliente com conhecimento RTF chamar [RTFSync.](rtfsync.md) 
  
A maioria dos armazenamentos de mensagens com conhecimento RTF não recebe o texto da mensagem por clientes; ele deve ser calculado 24 horas por solicitação. Como esse cálculo é demorado e caro, os clientes devem PR_RTF_COMPRESSED **sempre** que possível. Para calcular a **PR_BODY,** o provedor de armazenamento de mensagens deve descompactar o conteúdo da propriedade **PR_RTF_COMPRESSED** e remover a formatação rich text. Clientes que não suportam a **propriedade PR_RTF_COMPRESSED** exigem que esse cálculo seja realizado para cada mensagem. 
  
Ao copiar mensagens, os provedores de armazenamento de mensagens que não usam os métodos **IMAPISupport::D oCopyProps** ou **IMAPISupport::D oCopyTo** correrão o risco de criar uma mensagem sem conteúdo se sua implementação excluir a propriedade **PR_BODY** e se basear em **PR_RTF_COMPRESSED**. É possível que os dados na propriedade **PR_RTF_COMPRESSED** sejam corrompidos. Antes de excluir qualquer uma dessas propriedades de conteúdo de mensagem na operação de cópia, verifique se há corrupção da seguinte forma: 
  
1. Se o valor de **PR_RTF_COMPRESSED** não for maior que o RTF compactado, a propriedade está corrompida. 
    
2. Se o valor mágico no header RTF não for  _dwMagicCompressedRTF_ ou  _dwMagicUncompressedRTF,_ a propriedade está corrompida.
    
Os provedores de armazenamento de mensagens que usam os métodos de suporte não precisam se preocupar com a implementação de uma verificação de PR_RTF_COMPRESSED **corrupção;** O MAPI garante que as propriedades apropriadas existam e sejam válidas. 
  
Há três níveis diferentes de suporte ATF que os provedores de armazenamento de mensagens podem implementar; A MAPI recomenda que provedores de armazenamento de mensagens com suporte a RTF implementem seu suporte no nível médio ou superior. Todos os provedores de armazenamento de mensagens com conhecimento de RTF cuidam da geração de **PR_BODY** a partir dos dados incluídos no **PR_RTF_COMPRESSED** em mensagens de saída e fazem uma chamada ao **RTFSync** para sincronizar texto e formatação em mensagens de entrada. 
  
As diferenças entre esses três níveis são descritas na tabela a seguir. 
  
|**Nível de suporte**|**Descrição**|
|:-----|:-----|
|Baixo  <br/> |O provedor de armazenamento de mensagens chama **o RTFSync** sempre que as alterações são salvas em uma mensagem e extrai os dados da propriedade **PR_BODY** do **PR_RTF_COMPRESSED** em vez de exigir que os clientes a deem. Os **PR_BODY** e **PR_RTF_COMPRESSED** são armazenados.  <br/> |
|Meio  <br/> |O provedor de armazenamento de mensagens armazena somente **a PR_RTF_COMPRESSED,** **calculando** PR_BODY quando necessário.  <br/> |
|Alto  <br/> |O provedor de armazenamento de mensagens **não PR_BODY** nem as propriedades auxiliares RTF. **O RTFSync** é chamado quando o texto da mensagem é alterado e a formatação permanece inalterada ou quando uma nova mensagem é baixada por um provedor de transporte.  <br/> |
   

