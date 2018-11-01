---
title: Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed450913c7512e8ef20983484ca4b874878fd791
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867164"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="38f8e-102">Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS</span><span class="sxs-lookup"><span data-stu-id="38f8e-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="38f8e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="38f8e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38f8e-104">Conta do servidor web anônima (IUSR\_*ComputerName*) devem ser adicionados para o grupo local convidados no computador do servidor web para usar o RDS.</span><span class="sxs-lookup"><span data-stu-id="38f8e-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="38f8e-105">**Para conceder privilégios de convidados a um computador servidor web**</span><span class="sxs-lookup"><span data-stu-id="38f8e-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="38f8e-106">No computador do servidor Microsoft Windows® 2000, clique em **Iniciar**, aponte para **Programas**, para **Ferramentas Administrativas** e, em seguida, clique em **Gerenciamento do Computador**.</span><span class="sxs-lookup"><span data-stu-id="38f8e-106">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="38f8e-107">Na árvore do console, em **Grupos e Usuários Locais**, clique em **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="38f8e-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="38f8e-p101">Selecione o grupo local **Convidados**. No menu **Ação**, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="38f8e-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="38f8e-110">Na caixa de diálogo **Propriedades dos Convidados**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="38f8e-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="38f8e-111">Se a conta do servidor de web anônimo não aparecer na lista da caixa de diálogo **Selecionar usuários ou grupos** , digite seu nome (IUSR\_*ComputerName*) na parte inferior em branco caixa e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="38f8e-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="38f8e-112">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="38f8e-112">Click **OK**.</span></span>

