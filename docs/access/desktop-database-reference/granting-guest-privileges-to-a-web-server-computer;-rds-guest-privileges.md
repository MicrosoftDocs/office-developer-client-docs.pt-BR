---
title: Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bee4c05e3adc0fa3ad722b5c82c63f315860e12c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604110"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="c6125-102">Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS</span><span class="sxs-lookup"><span data-stu-id="c6125-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="c6125-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6125-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6125-104"><<<<<<< A conta do servidor Web anônima de cabeçalho (IUSR\_*ComputerName*) devem ser adicionados para o grupo local convidados no computador do servidor Web para usar o RDS.</span><span class="sxs-lookup"><span data-stu-id="c6125-104"><<<<<<< HEAD The anonymous Web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the Web server computer to use RDS.</span></span>

<a name="to-grant-guest-privileges-to-a-web-server-computer"></a><span data-ttu-id="c6125-105">**Para conceder privilégios de convidados a um computador do servidor Web**</span><span class="sxs-lookup"><span data-stu-id="c6125-105">**To grant guest privileges to a Web server computer**</span></span>
=======
<span data-ttu-id="c6125-106">Conta do servidor web anônima (IUSR\_*ComputerName*) devem ser adicionados para o grupo local convidados no computador do servidor web para usar o RDS.</span><span class="sxs-lookup"><span data-stu-id="c6125-106">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="c6125-107">**Para conceder privilégios de convidados a um computador servidor web**</span><span class="sxs-lookup"><span data-stu-id="c6125-107">**To grant guest privileges to a web server computer**</span></span>
>>>>>>> <span data-ttu-id="c6125-108">mestre</span><span class="sxs-lookup"><span data-stu-id="c6125-108">master</span></span>

1.  <span data-ttu-id="c6125-109">No computador do servidor Microsoft Windows® 2000, clique em **Iniciar**, aponte para **Programas**, para **Ferramentas Administrativas** e, em seguida, clique em **Gerenciamento do Computador**.</span><span class="sxs-lookup"><span data-stu-id="c6125-109">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="c6125-110">Na árvore do console, em **Grupos e Usuários Locais**, clique em **Grupos**.</span><span class="sxs-lookup"><span data-stu-id="c6125-110">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="c6125-p101">Selecione o grupo local **Convidados**. No menu **Ação**, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="c6125-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="c6125-113">Na caixa de diálogo **Propriedades dos Convidados**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="c6125-113">In the **Guests Properties** dialog box, click **Add**.</span></span>

<span data-ttu-id="c6125-114"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c6125-114"><<<<<<< HEAD</span></span>
5.  <span data-ttu-id="c6125-115">Se a conta do servidor Web anônima não aparecer na lista da caixa de diálogo **Selecionar usuários ou grupos** , digite seu nome (IUSR\_*ComputerName*) na parte inferior em branco caixa e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="c6125-115">If the anonymous Web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>
=======
5.  <span data-ttu-id="c6125-116">Se a conta do servidor de web anônimo não aparecer na lista da caixa de diálogo **Selecionar usuários ou grupos** , digite seu nome (IUSR\_*ComputerName*) na parte inferior em branco caixa e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="c6125-116">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>
>>>>>>> <span data-ttu-id="c6125-117">mestre</span><span class="sxs-lookup"><span data-stu-id="c6125-117">master</span></span>

6.  <span data-ttu-id="c6125-118">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6125-118">Click **OK**.</span></span>

