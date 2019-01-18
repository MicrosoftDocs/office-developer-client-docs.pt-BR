---
title: Concedendo privilégios de convidados a um computador do servidor web; Privilégios de convidados RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700546"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="bfe0b-102">Concedendo privilégios de convidados a um computador do servidor web; Privilégios de convidados RDS</span><span class="sxs-lookup"><span data-stu-id="bfe0b-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="bfe0b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfe0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bfe0b-104">Conta do servidor web anônima (IUSR\_*ComputerName*) devem ser adicionados para o grupo local convidados no computador do servidor web para usar o RDS.</span><span class="sxs-lookup"><span data-stu-id="bfe0b-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="bfe0b-105">**Para conceder privilégios de convidados a um computador servidor web**</span><span class="sxs-lookup"><span data-stu-id="bfe0b-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="bfe0b-106">No computador do Microsoft Windows 2000 Server, clique em **Iniciar**, aponte para **programas**, aponte para **Ferramentas administrativas**e, em seguida, clique em **Gerenciamento do computador**.</span><span class="sxs-lookup"><span data-stu-id="bfe0b-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="bfe0b-107">Na árvore do console, em **Grupos e Usuários Locais**, clique em **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="bfe0b-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="bfe0b-p101">Selecione o grupo local **Convidados**. No menu **Ação**, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="bfe0b-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="bfe0b-110">Na caixa de diálogo **Propriedades dos Convidados**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="bfe0b-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="bfe0b-111">Se a conta do servidor de web anônimo não aparecer na lista da caixa de diálogo **Selecionar usuários ou grupos** , digite seu nome (IUSR\_*ComputerName*) na parte inferior em branco caixa e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="bfe0b-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="bfe0b-112">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="bfe0b-112">Click **OK**.</span></span>

