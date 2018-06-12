---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Retorna o nome para exibição da conta que entregar a mensagem.
ms.openlocfilehash: 223bc5bbd485426676376d94875274613ff59685
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766054"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Retorna o nome para exibição da conta que entregar a mensagem.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidInetAcctName  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x00008580  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa propriedade deve conter o mesmo valor que é retornado da propriedade API de gerenciamento de conta [PROP_ACCT_NAME](prop_acct_name.md) para a conta que entregar a mensagem. 
  
Provedores de armazenamento de mensagem exponham essa propriedade nomeada e [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) para que ocorrem as seguintes ações: 
  
- Quando um usuário clica **responder a todos** em uma mensagem de email, o Outlook remove o endereço de email que está associado à conta e é marcado em mensagem da lista de destinatários da resposta. Esse comportamento ocorre, a menos que esse endereço de email é o remetente da mensagem original. 
    
- Por padrão, o Outlook envia respostas e encaminhadas através da conta que é marcada na mensagem original.
    
Em geral, o gerente de protocolo do Outlook entrega de mensagens e Outlook define as propriedades **PidLidInternetAccountName** e **PidLidInternetAccountStamp** para indicar a conta que entregar a mensagem. No entanto, se um armazenamento de mensagens está intimamente ligado com um transporte, o gerente de protocolo do Outlook não entregar mensagens e o Outlook não pode definir essas propriedades. Neste cenário, o Outlook chama a função [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) . Se o provedor de armazenamento de mensagem deseja expor essas propriedades nomeadas, ele deve implementar **IMAPIProp::GetIDsFromNames** e retornar as marcas de propriedade por meio do parâmetro de saída *lppPropTags* . Outlook, chame o método [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) usando essas marcas da propriedade e o provedor de armazenamento de mensagens pode retornar o nome da conta e o carimbo da conta desejada. 
  
Para oferecer suporte a essas propriedades nomeadas, provedores de armazenamento devem esperar que o Outlook para usar **IMAPIProp::GetIDsFromNames** para obter a marca de propriedade para essa propriedade. Outlook Especifica os seguintes valores para a estrutura [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) que corresponde a essa propriedade nomeada, que é passada como parte da matriz apontada pelo parâmetro de entrada *lppPropNames* do **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)
- [Propriedade canônico de PidLidInternetAccountName](http://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

