---
title: Contas
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d539f38419a8eaac60cd3054da6283a49bf4cc00
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723009"
---
# <a name="accounts"></a>Contas 

Esta seção fornece tarefas de exemplo que envolvem contas de email. Como exemplos de contas de email temos o Microsoft Exchange Server, POP3, IMAP e HTTP. Uma conta do perfil atual é representada por um objeto [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).


|Tópico|Descrição|
|:----|:----------|
|[Obter informações da conta](how-to-get-account-information.md) | Aceita como um argumento de entrada um objeto [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) confiável do Microsoft Outlook e usa o objeto **Account** para exibir os detalhes de cada conta que está disponível para o perfil do Outlook atual.|
|[Criar um item enviável para uma conta específica com base na pasta atual](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | Inclui dois exemplos de código que mostram como criar um item de email e solicitação de reunião enviáveis e enviá-los usando uma conta específica baseada na pasta atual.|
|[Obter a conta de uma pasta](how-to-get-the-account-for-a-folder.md) | Obtém a conta que está associada a uma pasta na sessão atual.|
|[Obter informações sobre várias contas](how-to-get-information-about-multiple-accounts.md) | Obtém e exibe diversas informações sobre cada conta no perfil atual.|
|[Enviar um item de email usando uma conta do Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | Usa a propriedade [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) para enviar um item de email usando uma conta do Windows Live Hotmail.|

## <a name="see-also"></a>Confira também

- [Usuários do Exchange](exchange-users.md)
- [Email](mail.md)
- [Destinatários](recipients.md)
- [Como faço para... (Referência do Outlook 2013 PIA)](how-do-i-outlook-2013-pia-reference.md)

