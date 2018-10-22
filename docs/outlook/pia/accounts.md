---
title: Contas
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: eb7c56a8a261f36628c3b440c1aeec31c7aec46e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406817"
---
# <a name="accounts"></a><span data-ttu-id="8e7fd-102">Contas</span><span class="sxs-lookup"><span data-stu-id="8e7fd-102">Accounts</span></span> 

<span data-ttu-id="8e7fd-103">Esta seção fornece tarefas de exemplo que envolvem contas de email.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-103">This section provides sample tasks that involve email accounts.</span></span> <span data-ttu-id="8e7fd-104">Como exemplos de contas de email temos o Microsoft Exchange Server, POP3, IMAP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-104">Examples of email accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts.</span></span> <span data-ttu-id="8e7fd-105">Uma conta do perfil atual é representada por um objeto [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="8e7fd-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="8e7fd-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="8e7fd-106">Topic</span></span>|<span data-ttu-id="8e7fd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e7fd-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="8e7fd-108">Obter informações da conta</span><span class="sxs-lookup"><span data-stu-id="8e7fd-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="8e7fd-109">Aceita como um argumento de entrada um objeto [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) confiável do Microsoft Outlook e usa o objeto **Account** para exibir os detalhes de cada conta que está disponível para o perfil do Outlook atual.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-109">The  method takes as an input argument a trusted Outlook[Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="8e7fd-110">Criar um item enviável para uma conta específica com base na pasta atual</span><span class="sxs-lookup"><span data-stu-id="8e7fd-110">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="8e7fd-111">Inclui dois exemplos de código que mostram como criar um item de email e solicitação de reunião enviáveis e enviá-los usando uma conta específica baseada na pasta atual.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-111">Contains two code examples that show how to create a sendable email item and meeting request, and then send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="8e7fd-112">Obter a conta de uma pasta</span><span class="sxs-lookup"><span data-stu-id="8e7fd-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="8e7fd-113">Obtém a conta que está associada a uma pasta na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="8e7fd-114">Obter informações sobre várias contas</span><span class="sxs-lookup"><span data-stu-id="8e7fd-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="8e7fd-115">Obtém e exibe diversas informações sobre cada conta no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|[<span data-ttu-id="8e7fd-116">Enviar um item de email usando uma conta do Hotmail</span><span class="sxs-lookup"><span data-stu-id="8e7fd-116">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | <span data-ttu-id="8e7fd-117">Usa a propriedade [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) para enviar um item de email usando uma conta do Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-117">Uses the [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="8e7fd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e7fd-118">See also</span></span>

- [<span data-ttu-id="8e7fd-119">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="8e7fd-119">Exchange users</span></span>](exchange-users.md)
- [<span data-ttu-id="8e7fd-120">Email</span><span class="sxs-lookup"><span data-stu-id="8e7fd-120">mail</span></span>](mail.md)
- [<span data-ttu-id="8e7fd-121">Destinatários</span><span class="sxs-lookup"><span data-stu-id="8e7fd-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="8e7fd-122">Como faço para... (Referência do Outlook 2013 PIA)</span><span class="sxs-lookup"><span data-stu-id="8e7fd-122">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

