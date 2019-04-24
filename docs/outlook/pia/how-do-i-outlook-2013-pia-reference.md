---
title: Como faço para... (Referência do Outlook 2013 PIA)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bc4e19271e2747f5ffa8586b9f2ab226d6658b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355794"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a><span data-ttu-id="b6bf0-102">Como faço para... (Referência do Outlook 2013 PIA)</span><span class="sxs-lookup"><span data-stu-id="b6bf0-102">How do I... (Outlook 2013 PIA reference)</span></span>

<span data-ttu-id="b6bf0-103">Esta seção contém tópicos de tarefas e exemplos de código no Visual Basic e C\# que demonstram como fazer algumas tarefas comuns no Outlook.</span><span class="sxs-lookup"><span data-stu-id="b6bf0-103">This section contains procedural tasks topics and code examples in Visual Basic and C\# that demonstrate how to perform some common tasks in Outlook.</span></span>

<span data-ttu-id="b6bf0-104">Para executar esses exemplos de código, você deve ter instalado as versões Outlook 2010 e o Visual Studio 2008 ou versões posteriores desses produtos.</span><span class="sxs-lookup"><span data-stu-id="b6bf0-104">To run these code examples, you must have installed Outlook 2010 and Visual Studio 2008, or a later version of these products.</span></span>

<span data-ttu-id="b6bf0-105">Os exemplos de código desta seção não exigem que você instale ferramentas de desenvolvedor do Office para o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b6bf0-105">The code examples in this section do not require that you have installed Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="b6bf0-106">No entanto, você pode consultar o portal [Introdução ao desenvolvimento do Office](https://developer.microsoft.com/office/docs) para obter informações sobre como usar as ferramentas e consultar[soluções Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) para algumas tarefas básicas de como escrever no código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b6bf0-106">However, you can refer to the [Getting started with Office development](https://developer.microsoft.com/office/docs) portal for information about using the tools, and refer to [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) for some basic how-to tasks written in managed code.</span></span>

<span data-ttu-id="b6bf0-107">Exemplo de código nesse intervalo de seção do nível iniciante ao avançado, e alguns deles são adaptados do catálogo [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b6bf0-107">Code examples in this section range from the beginner to the intermediate levels, and some of them are adapted from the book [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span></span>

<span data-ttu-id="b6bf0-108">A equipe da Documentação do Office dá as boas vindas aos seus exemplos de código e ideias de tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6bf0-108">The Office Developer Documentation team welcomes your task ideas and code samples.</span></span> <span data-ttu-id="b6bf0-109">Se usarmos suas amostras de código no conteúdo do Outlook, reconhecemos seu trabalho com um subtítulo e um link para seu site.</span><span class="sxs-lookup"><span data-stu-id="b6bf0-109">If we use your code samples in Outlook content, we will recognize your work with a byline and a link to your website.</span></span> <span data-ttu-id="b6bf0-110">Para saber mais, contate-no docthis@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b6bf0-110">For more information, contact us at docthis@microsoft.com.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6bf0-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b6bf0-111">In this section</span></span> 

[<span data-ttu-id="b6bf0-112">Contas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-112">Accounts</span></span>](accounts.md)

- [<span data-ttu-id="b6bf0-113">Obter informações da conta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-113">Get account information</span></span>](how-to-get-account-information.md)
- [<span data-ttu-id="b6bf0-114">Criar um item enviável para uma conta específica com base na pasta atual</span><span class="sxs-lookup"><span data-stu-id="b6bf0-114">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [<span data-ttu-id="b6bf0-115">Obter a conta de uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-115">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md)
- [<span data-ttu-id="b6bf0-116">Obter informações sobre várias contas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-116">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md)
- [<span data-ttu-id="b6bf0-117">Enviar um item de email usando uma conta do Hotmail</span><span class="sxs-lookup"><span data-stu-id="b6bf0-117">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[<span data-ttu-id="b6bf0-118">Suplemento de administração</span><span class="sxs-lookup"><span data-stu-id="b6bf0-118">Add-in administration</span></span>](add-in-administration.md)

- [<span data-ttu-id="b6bf0-119">Determinar se o Outlook é um aplicativo Clique para Executar em um computador</span><span class="sxs-lookup"><span data-stu-id="b6bf0-119">Determine whether Outlook is a Click-to-Run application on a computer</span></span>](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[<span data-ttu-id="b6bf0-120">Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="b6bf0-120">Address book</span></span>](address-book.md)

- [<span data-ttu-id="b6bf0-121">Exibir na caixa de diálogo Escolher nomes no catálogo de endereços que corresponde a uma pasta Contatos</span><span class="sxs-lookup"><span data-stu-id="b6bf0-121">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [<span data-ttu-id="b6bf0-122">Obter a Lista de Endereços Global ou um conjunto de listas de endereços de um repositório</span><span class="sxs-lookup"><span data-stu-id="b6bf0-122">Get the Global Address List or a set of address lists for a store</span></span>](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [<span data-ttu-id="b6bf0-123">Enumerar as entradas na Lista de Endereços Global</span><span class="sxs-lookup"><span data-stu-id="b6bf0-123">Enumerate the entries in the Global Address List</span></span>](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [<span data-ttu-id="b6bf0-124">Exibir listas de endereços para um perfil</span><span class="sxs-lookup"><span data-stu-id="b6bf0-124">Display the address lists for a profile</span></span>](how-to-display-the-address-lists-for-a-profile.md)

[<span data-ttu-id="b6bf0-125">Compromissos</span><span class="sxs-lookup"><span data-stu-id="b6bf0-125">Appointments</span></span>](appointments.md)

- [<span data-ttu-id="b6bf0-126">Criar um compromisso que é um evento de dia inteiro</span><span class="sxs-lookup"><span data-stu-id="b6bf0-126">Create an appointment that is an all-day event</span></span>](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [<span data-ttu-id="b6bf0-127">Criar um compromisso que inicia no Fuso Horário do Pacífico e termina no Fuso Horário da Costa Leste</span><span class="sxs-lookup"><span data-stu-id="b6bf0-127">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [<span data-ttu-id="b6bf0-128">Especificar tipos diferentes de destinatários para um item de compromisso</span><span class="sxs-lookup"><span data-stu-id="b6bf0-128">Specify different recipient types for an appointment item</span></span>](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [<span data-ttu-id="b6bf0-129">Criar um compromisso recorrente que usa o padrão de recorrência padrão</span><span class="sxs-lookup"><span data-stu-id="b6bf0-129">Create a recurring appointment by using the default recurrence pattern</span></span>](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [<span data-ttu-id="b6bf0-130">Criar um compromisso recorrente com um padrão semanal</span><span class="sxs-lookup"><span data-stu-id="b6bf0-130">Create a recurring appointment that has a weekly pattern</span></span>](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [<span data-ttu-id="b6bf0-131">Criar um compromisso recorrente anual com um padrão de YearNth</span><span class="sxs-lookup"><span data-stu-id="b6bf0-131">Create an annual recurring appointment that uses a YearNth pattern</span></span>](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [<span data-ttu-id="b6bf0-132">Localizar um compromisso específico em uma série de compromissos recorrentes</span><span class="sxs-lookup"><span data-stu-id="b6bf0-132">Find a specific appointment in a recurring appointment series</span></span>](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="b6bf0-133">Criar um compromisso de exceção em uma série de compromisso recorrente</span><span class="sxs-lookup"><span data-stu-id="b6bf0-133">Create an exception appointment in a recurring appointment series</span></span>](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="b6bf0-134">Criar um lembrete para um item de compromisso</span><span class="sxs-lookup"><span data-stu-id="b6bf0-134">Create a reminder for an appointment item</span></span>](how-to-create-a-reminder-for-an-appointment-item.md)
- [<span data-ttu-id="b6bf0-135">Importar dados XML de compromisso para objetos de compromisso do Outlook</span><span class="sxs-lookup"><span data-stu-id="b6bf0-135">Import appointment XML data into Outlook appointment objects</span></span>](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[<span data-ttu-id="b6bf0-136">Anexos</span><span class="sxs-lookup"><span data-stu-id="b6bf0-136">Attachments</span></span>](attachments.md)

- [<span data-ttu-id="b6bf0-137">Anexar um arquivo a um item de email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-137">Attach a file to a mail item</span></span>](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [<span data-ttu-id="b6bf0-138">Anexar um item de Contato do Outlook a uma mensagem de email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-138">Attach an Outlook Contact item to an email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [<span data-ttu-id="b6bf0-139">Limitar o tamanho de um anexo para uma mensagem de email do Outlook</span><span class="sxs-lookup"><span data-stu-id="b6bf0-139">Limit the size of an attachment to an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [<span data-ttu-id="b6bf0-140">Modificar um anexo de uma mensagem de email do Outlook</span><span class="sxs-lookup"><span data-stu-id="b6bf0-140">Modify an attachment of an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [<span data-ttu-id="b6bf0-141">Remover os anexos de nível 2 de segurança de mensagens e salvá-los no disco por programação</span><span class="sxs-lookup"><span data-stu-id="b6bf0-141">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[<span data-ttu-id="b6bf0-142">Calendar</span><span class="sxs-lookup"><span data-stu-id="b6bf0-142">Calendar</span></span>](calendar.md)

- [<span data-ttu-id="b6bf0-143">Compartilhar cronograma de disponibilidade em um período específico de um calendário</span><span class="sxs-lookup"><span data-stu-id="b6bf0-143">Share Free/Busy schedule within a specified period in a calendar</span></span>](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [<span data-ttu-id="b6bf0-144">Compartilhar informações de calendário por email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-144">Share calendar information through email</span></span>](how-to-share-calendar-information-through-e-mail.md)
- [<span data-ttu-id="b6bf0-145">Exibir um calendário compartilhado de um destinatário</span><span class="sxs-lookup"><span data-stu-id="b6bf0-145">Display a shared calendar of a recipient</span></span>](how-to-display-a-shared-calendar-of-a-recipient.md)
- [<span data-ttu-id="b6bf0-146">Salvar um calendário no disco</span><span class="sxs-lookup"><span data-stu-id="b6bf0-146">Save a calendar to disk</span></span>](how-to-save-a-calendar-to-disk.md)
- [<span data-ttu-id="b6bf0-147">Abrir e exibir o conteúdo de um arquivo iCalendar</span><span class="sxs-lookup"><span data-stu-id="b6bf0-147">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[<span data-ttu-id="b6bf0-148">Categorias de cor</span><span class="sxs-lookup"><span data-stu-id="b6bf0-148">Color categories</span></span>](color-categories.md)

- [<span data-ttu-id="b6bf0-149">Enumerar e adicionar categorias</span><span class="sxs-lookup"><span data-stu-id="b6bf0-149">Enumerate and add categories</span></span>](how-to-enumerate-and-add-categories.md)
- [<span data-ttu-id="b6bf0-150">Atribuir categorias a um item</span><span class="sxs-lookup"><span data-stu-id="b6bf0-150">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)

[<span data-ttu-id="b6bf0-151">Contatos</span><span class="sxs-lookup"><span data-stu-id="b6bf0-151">Contacts</span></span>](contacts.md)

- [<span data-ttu-id="b6bf0-152">Criar um item de contato</span><span class="sxs-lookup"><span data-stu-id="b6bf0-152">Create a Contact item</span></span>](how-to-create-a-contact-item.md)
- [<span data-ttu-id="b6bf0-153">Criar um item de contato personalizado</span><span class="sxs-lookup"><span data-stu-id="b6bf0-153">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)
- [<span data-ttu-id="b6bf0-154">Criar um item de contato de um arquivo vCard e salvar o item em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-154">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[<span data-ttu-id="b6bf0-155">Conversas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-155">Conversations</span></span>](conversations.md)

- [<span data-ttu-id="b6bf0-156">Obter e exibir itens em uma conversa</span><span class="sxs-lookup"><span data-stu-id="b6bf0-156">Get and display items in a conversation</span></span>](how-to-get-and-display-items-in-a-conversation.md)
- [<span data-ttu-id="b6bf0-157">Obter e enumerar conversas selecionadas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-157">Get and enumerate selected conversations</span></span>](how-to-get-and-enumerate-selected-conversations.md)

[<span data-ttu-id="b6bf0-158">Cartões de visita eletrônicos</span><span class="sxs-lookup"><span data-stu-id="b6bf0-158">Electronic business cards</span></span>](electronic-business-cards.md)

- [<span data-ttu-id="b6bf0-159">Modificar o layout de um cartão de visita eletrônico</span><span class="sxs-lookup"><span data-stu-id="b6bf0-159">Modify the layout of an electronic business card</span></span>](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [<span data-ttu-id="b6bf0-160">Enviar um item de email com um cartão de visita eletrônico</span><span class="sxs-lookup"><span data-stu-id="b6bf0-160">Send a mail item with an electronic business card</span></span>](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[<span data-ttu-id="b6bf0-161">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="b6bf0-161">Exchange users</span></span>](exchange-users.md)

- [<span data-ttu-id="b6bf0-162">Acessar informações sobre o usuário atual</span><span class="sxs-lookup"><span data-stu-id="b6bf0-162">Get information about the current user</span></span>](how-to-get-information-about-the-current-user.md)
- [<span data-ttu-id="b6bf0-163">Obter informações sobre todas as listas de distribuição das quais o usuário atual participa</span><span class="sxs-lookup"><span data-stu-id="b6bf0-163">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [<span data-ttu-id="b6bf0-164">Criar uma lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="b6bf0-164">Create a distribution list</span></span>](how-to-create-a-distribution-list.md)
- [<span data-ttu-id="b6bf0-165">Obter membros de uma lista de distribuição do Exchange</span><span class="sxs-lookup"><span data-stu-id="b6bf0-165">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)
- [<span data-ttu-id="b6bf0-166">Acessar informações sobre o gerente do usuário atual</span><span class="sxs-lookup"><span data-stu-id="b6bf0-166">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)
- [<span data-ttu-id="b6bf0-167">Ter informações de disponibilidade do gerente de um usuário Exchange</span><span class="sxs-lookup"><span data-stu-id="b6bf0-167">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [<span data-ttu-id="b6bf0-168">Verificar a resposta do gerente para uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="b6bf0-168">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [<span data-ttu-id="b6bf0-169">Obter informações sobre subordinados diretos do gerente do usuário atual </span><span class="sxs-lookup"><span data-stu-id="b6bf0-169">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[<span data-ttu-id="b6bf0-170">Pastas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-170">Folders</span></span>](folders.md)

- [<span data-ttu-id="b6bf0-171">Adicionar uma pasta à lista de pastas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-171">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md)
- [<span data-ttu-id="b6bf0-172">Enumerar pastas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-172">Enumerate folders</span></span>](how-to-enumerate-folders.md)
- [<span data-ttu-id="b6bf0-173">Obter uma pasta padrão e enumerar suas subpastas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-173">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [<span data-ttu-id="b6bf0-174">Obter uma pasta com base em seu caminho de pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-174">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)
- [<span data-ttu-id="b6bf0-175">Selecionar uma pasta e exibir informações de pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-175">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)
- [<span data-ttu-id="b6bf0-176">Obter a classe de mensagens padrão de uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-176">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)
- [<span data-ttu-id="b6bf0-177">Acessar dados específicos da solução armazenados como uma mensagem oculta em uma pasta </span><span class="sxs-lookup"><span data-stu-id="b6bf0-177">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [<span data-ttu-id="b6bf0-178">Certifique-se de que as propriedades de item personalizadas são compatíveis com consultas ao nível de pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-178">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[<span data-ttu-id="b6bf0-179">Itens gerais do Outlook</span><span class="sxs-lookup"><span data-stu-id="b6bf0-179">General Outlook items</span></span>](general-outlook-items.md)

- [<span data-ttu-id="b6bf0-180">Criar uma classe auxiliar para acessar membros comuns do item do Outlook</span><span class="sxs-lookup"><span data-stu-id="b6bf0-180">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="b6bf0-181">Exibir itens selecionados no Explorer ativo</span><span class="sxs-lookup"><span data-stu-id="b6bf0-181">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)

[<span data-ttu-id="b6bf0-182">Compartilhamento de grupo</span><span class="sxs-lookup"><span data-stu-id="b6bf0-182">Group sharing</span></span>](group-sharing.md)

- [<span data-ttu-id="b6bf0-183">Assinar um RSS feed</span><span class="sxs-lookup"><span data-stu-id="b6bf0-183">Subscribe to an RSS feed</span></span>](how-to-subscribe-to-an-rss-feed.md)
- [<span data-ttu-id="b6bf0-184">Sincroniza o Outlook com uma pasta do SharePoint</span><span class="sxs-lookup"><span data-stu-id="b6bf0-184">Synchronize Outlook with a SharePoint folder</span></span>](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[<span data-ttu-id="b6bf0-185">Email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-185">Mail</span></span>](mail.md)

- [<span data-ttu-id="b6bf0-186">Criar um item de email usando um modelo de mensagem</span><span class="sxs-lookup"><span data-stu-id="b6bf0-186">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)
- [<span data-ttu-id="b6bf0-187">Criar um item de email, anexa um relatório e envia o item de email ao gerente do usuário</span><span class="sxs-lookup"><span data-stu-id="b6bf0-187">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [<span data-ttu-id="b6bf0-188">Enviar um email com o endereço SMTP de uma conta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-188">Send an email given the SMTP address of an account</span></span>](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [<span data-ttu-id="b6bf0-189">Adicionar opções de votação para um item de email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-189">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md)
- [<span data-ttu-id="b6bf0-190">Adicionar uma ação personalizada como resposta a um item de email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-190">Add a custom action as a response to a mail item</span></span>](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [<span data-ttu-id="b6bf0-191">Obter o endereço SMTP do remetente de um item de email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-191">Get the SMTP address of the sender of a mail item</span></span>](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [<span data-ttu-id="b6bf0-192">Especificar tipos diferentes de destinatários para um item de email</span><span class="sxs-lookup"><span data-stu-id="b6bf0-192">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md)

[<span data-ttu-id="b6bf0-193">Solicitações de reunião</span><span class="sxs-lookup"><span data-stu-id="b6bf0-193">Meeting requests</span></span>](meeting-requests.md)

- [<span data-ttu-id="b6bf0-194">Criar uma solicitação de reunião, adicionar destinatários e especificar um local</span><span class="sxs-lookup"><span data-stu-id="b6bf0-194">Create a meeting request, add recipients, and specify a location</span></span>](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [<span data-ttu-id="b6bf0-195">Obter o organizador de uma reunião</span><span class="sxs-lookup"><span data-stu-id="b6bf0-195">Get the organizer of a meeting</span></span>](how-to-get-the-organizer-of-a-meeting.md)
- [<span data-ttu-id="b6bf0-196">Verificar todas as respostas à solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="b6bf0-196">Check all responses to a meeting request</span></span>](how-to-check-all-responses-to-a-meeting-request.md)
- [<span data-ttu-id="b6bf0-197">Localizar o item de compromisso associado a uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="b6bf0-197">Find the appointment item associated with a meeting request</span></span>](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [<span data-ttu-id="b6bf0-198">Aceitar automaticamente uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="b6bf0-198">Automatically accept a meeting request</span></span>](how-to-automatically-accept-a-meeting-request.md)
- [<span data-ttu-id="b6bf0-199">Solicitar que um usuário responda a uma solicitação de reunião</span><span class="sxs-lookup"><span data-stu-id="b6bf0-199">Prompt a user to respond to a meeting request</span></span>](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[<span data-ttu-id="b6bf0-200">Destinatários</span><span class="sxs-lookup"><span data-stu-id="b6bf0-200">Recipients</span></span>](recipients.md)

- [<span data-ttu-id="b6bf0-201">Exibir a caixa de diálogo Escolher nomes para resolver os destinatários</span><span class="sxs-lookup"><span data-stu-id="b6bf0-201">Display the Select Names dialog box to resolve recipients</span></span>](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [<span data-ttu-id="b6bf0-202">Usar a caixa de diálogo Escolher nomes para receber e atribuir destinatários a um compromisso</span><span class="sxs-lookup"><span data-stu-id="b6bf0-202">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [<span data-ttu-id="b6bf0-203">Receber o endereço de email de um destinatário</span><span class="sxs-lookup"><span data-stu-id="b6bf0-203">Get the email address of a recipient</span></span>](how-to-get-the-e-mail-address-of-a-recipient.md)

[<span data-ttu-id="b6bf0-204">Regras</span><span class="sxs-lookup"><span data-stu-id="b6bf0-204">Rules</span></span>](rules.md)

- [<span data-ttu-id="b6bf0-205">Criar uma regra para itens de email do arquivo de um gerente e sinalizá-la para acompanhamento</span><span class="sxs-lookup"><span data-stu-id="b6bf0-205">Create a rule to file mail items from a manager and flag them for follow-up</span></span>](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [<span data-ttu-id="b6bf0-206">Executar uma regra instantaneamente</span><span class="sxs-lookup"><span data-stu-id="b6bf0-206">Execute a rule instantly</span></span>](how-to-execute-a-rule-instantly.md)
- [<span data-ttu-id="b6bf0-207">Executar uma regra em um computador local</span><span class="sxs-lookup"><span data-stu-id="b6bf0-207">Execute a rule on a local computer</span></span>](how-to-execute-a-rule-on-a-local-computer.md)
- [<span data-ttu-id="b6bf0-208">Criar uma regra para atribuir categorias a itens de email com base em várias palavras utilizadas no assunto</span><span class="sxs-lookup"><span data-stu-id="b6bf0-208">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[<span data-ttu-id="b6bf0-209">Amostras de tarefas usando eventos do Outlook</span><span class="sxs-lookup"><span data-stu-id="b6bf0-209">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

- [<span data-ttu-id="b6bf0-210">Implementar um invólucro para inspetores e rastrear eventos em nível de item em cada inspetor</span><span class="sxs-lookup"><span data-stu-id="b6bf0-210">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[<span data-ttu-id="b6bf0-211">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="b6bf0-211">Search and filter</span></span>](search-and-filter.md)

- [<span data-ttu-id="b6bf0-212">Filtrar e enumerar de forma eficiente itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-212">Filter and efficiently enumerate items in a folder</span></span>](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="b6bf0-213">Usar SetColumns para enumerar itens de forma eficiente em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-213">Use SetColumns to efficiently enumerate items in a folder</span></span>](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="b6bf0-214">Usar matrizes para enumerar itens em uma pasta com eficiência</span><span class="sxs-lookup"><span data-stu-id="b6bf0-214">Use arrays to efficiently enumerate items in a folder</span></span>](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="b6bf0-215">Enumerar itens na Caixa de Entrada com base na hora da última modificação</span><span class="sxs-lookup"><span data-stu-id="b6bf0-215">Enumerate items in the Inbox based on the last modification time</span></span>](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [<span data-ttu-id="b6bf0-216">Filtrar e exibir os itens de Caixa de Entrada modificados no mês passado</span><span class="sxs-lookup"><span data-stu-id="b6bf0-216">Filter and display Inbox items modified in the last month</span></span>](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [<span data-ttu-id="b6bf0-217">Filtrar e exibir propriedades de valores múltiplos ao enumerar itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-217">Filter and display multivalued properties when enumerating items in a folder</span></span>](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="b6bf0-218">Filtrar e exibir propriedades computadas ao enumerar itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-218">Filter and display computed properties when enumerating items in a folder</span></span>](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="b6bf0-219">Enumerar itens ocultos em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-219">Enumerate hidden items in a folder</span></span>](how-to-enumerate-hidden-items-in-a-folder.md)
- [<span data-ttu-id="b6bf0-220">Use a pesquisa instantânea para pesquisar por uma frase em todas as pastas e repositórios no assunto</span><span class="sxs-lookup"><span data-stu-id="b6bf0-220">Use instant search to search all folders and all stores for a phrase in the subject</span></span>](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [<span data-ttu-id="b6bf0-221">Procurar uma frase no corpo dos itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-221">Search for a phrase in the body of items in a folder</span></span>](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [<span data-ttu-id="b6bf0-222">Pesquisar por uma frase exata em anexos de itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="b6bf0-222">Search attachments of items in a folder for an exact phrase</span></span>](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [<span data-ttu-id="b6bf0-223">Pesquisar e obter compromissos em um intervalo de tempo</span><span class="sxs-lookup"><span data-stu-id="b6bf0-223">Search and obtain appointments in a time range</span></span>](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [<span data-ttu-id="b6bf0-224">Filtrar compromissos recorrentes e pesquisar por uma cadeia de caracteres no assunto</span><span class="sxs-lookup"><span data-stu-id="b6bf0-224">Filter recurring appointments and search for a string in the subject</span></span>](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [<span data-ttu-id="b6bf0-225">Pesquisar e obter itens em um modo de exibição agregado</span><span class="sxs-lookup"><span data-stu-id="b6bf0-225">Search and obtain items in an aggregated view</span></span>](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[<span data-ttu-id="b6bf0-226">Sessões</span><span class="sxs-lookup"><span data-stu-id="b6bf0-226">Sessions</span></span>](sessions.md)

- [<span data-ttu-id="b6bf0-227">Acessar e entrar em uma instância do Outlook</span><span class="sxs-lookup"><span data-stu-id="b6bf0-227">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[<span data-ttu-id="b6bf0-228">Repositórios</span><span class="sxs-lookup"><span data-stu-id="b6bf0-228">Stores</span></span>](stores.md)

- [<span data-ttu-id="b6bf0-229">Obter informações sobre repositórios em um perfil</span><span class="sxs-lookup"><span data-stu-id="b6bf0-229">Get information about stores in a profile</span></span>](how-to-get-information-about-stores-in-a-profile.md)
- [<span data-ttu-id="b6bf0-230">Adicionar ou remover um repositório</span><span class="sxs-lookup"><span data-stu-id="b6bf0-230">Add or remove a store</span></span>](how-to-add-or-remove-a-store.md)

[<span data-ttu-id="b6bf0-231">Tarefas</span><span class="sxs-lookup"><span data-stu-id="b6bf0-231">Tasks</span></span>](tasks.md)

- [<span data-ttu-id="b6bf0-232">Criar um item de tarefa</span><span class="sxs-lookup"><span data-stu-id="b6bf0-232">Create a task item</span></span>](how-to-create-a-task-item.md)
- [<span data-ttu-id="b6bf0-233">Atribuir uma tarefa a um destinatário</span><span class="sxs-lookup"><span data-stu-id="b6bf0-233">Assign a task to a recipient</span></span>](how-to-assign-a-task-to-a-recipient.md)
- [<span data-ttu-id="b6bf0-234">Exibir os itens de solicitação de tarefas enviados para um destinatário</span><span class="sxs-lookup"><span data-stu-id="b6bf0-234">Display the task request items sent to a recipient</span></span>](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [<span data-ttu-id="b6bf0-235">Responder a um item de solicitação de tarefa</span><span class="sxs-lookup"><span data-stu-id="b6bf0-235">Respond to a task request item</span></span>](how-to-respond-to-a-task-request-item.md)
- [<span data-ttu-id="b6bf0-236">Criar uma tarefa recorrente</span><span class="sxs-lookup"><span data-stu-id="b6bf0-236">Create a recurring task</span></span>](how-to-create-a-recurring-task.md)
- [<span data-ttu-id="b6bf0-237">Sinalizar itens de email de um gerente para acompanhamento</span><span class="sxs-lookup"><span data-stu-id="b6bf0-237">Flag mail items from a manager for follow-up</span></span>](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[<span data-ttu-id="b6bf0-238">Modos de exibição</span><span class="sxs-lookup"><span data-stu-id="b6bf0-238">Views</span></span>](views.md)

- [<span data-ttu-id="b6bf0-239">Criar um modo de exibição</span><span class="sxs-lookup"><span data-stu-id="b6bf0-239">Create a view</span></span>](how-to-create-a-view.md)
- [<span data-ttu-id="b6bf0-240">Adicionar campos a um modo de exibição</span><span class="sxs-lookup"><span data-stu-id="b6bf0-240">Add fields to a view</span></span>](how-to-add-fields-to-a-view.md)
- [<span data-ttu-id="b6bf0-241">Enumerar itens em um modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="b6bf0-241">Enumerate items in a table view</span></span>](how-to-enumerate-items-in-a-table-view.md)



