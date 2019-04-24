---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Retorna o nome de exibição da conta que entregou a mensagem.
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327682"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Retorna o nome de exibição da conta que entregou a mensagem.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidInetAcctName  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008580  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade deve conter o mesmo valor retornado da propriedade da API de Gerenciamento de Conta [PROP_ACCT_NAME](prop_acct_name.md) da conta que entregou a mensagem. 
  
Os provedores de repositórios de mensagens expõem esta propriedade nomeada e [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) para que ocorram as seguintes ações: 
  
- Quando um usuário clica em **Responder a Todos** em uma mensagem de email, o Outlook remove o endereço de email associado à conta e marcado na mensagem da lista de destinatários da resposta. Isso ocorre a menos que o endereço de email seja o remetente da mensagem original. 
    
- Por padrão, o Outlook envia respostas e mensagens encaminhadas por meio da conta que está marcada na mensagem original.
    
Normalmente, o Gerenciador de Protocolo do Outlook entrega as mensagens, e o Outlook configura as propriedades **PidLidInternetAccountName** e **PidLidInternetAccountStamp** para indicar a conta que entregou a mensagem. No entanto, se um repositório de mensagens estiver firmemente acoplado a um transporte, o Outlook Protocol Manager não entregará as mensagens e o Outlook não poderá definir essas propriedades. Nesse cenário, o Outlook chama a função [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx). Se o provedor de repositório de mensagens quiser expor essas propriedades nomeadas, deverá implementar **IMAPIProp::GetIDsFromNames** e retornar marcas de propriedade por meio do parâmetro de saída *lppPropTags* . O Outlook, em seguida, poderá chamar o método [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) usando essas marcas de propriedade, e o provedor de armazenamento de mensagens pode retornar o nome da conta e o carimbo da conta desejada. 
  
Para dar suporte a essas propriedades nomeadas, os provedores de repositórios devem esperar para usar o Outlook **IMAPIProp::GetIDsFromNames** para obter a marca de propriedade para esta propriedade. O Outlook especifica os seguintes valores para a estrutura [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx), que corresponde a esta propriedade nomeada, que é passada como parte da matriz apontada pelo parâmetro de entrada *lppPropNames* de ** IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)
- [Constantes (PI de gerenciamento de contas)](constants-account-management-api.md)
- [Propriedade canônica PidLidInternetAccountName](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

