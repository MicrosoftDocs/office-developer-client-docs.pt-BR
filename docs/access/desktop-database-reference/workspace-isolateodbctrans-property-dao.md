---
title: Propriedade Workspace.IsolateODBCTrans (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 197bf35c796fe1e34122b7d4214043e9217fb3d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878539"
---
# <a name="workspaceisolateodbctrans-property-dao"></a><span data-ttu-id="25f83-102">Propriedade Workspace.IsolateODBCTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="25f83-102">Workspace.IsolateODBCTrans Property (DAO)</span></span>


<span data-ttu-id="25f83-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="25f83-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25f83-104">Define ou retorna um valor que indica se vários transactiond, que envolvem o mesmo mecanismo do banco de dados do Microsoft Access conectado à fonte de dados ODBC, estão isolados (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="25f83-104">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="25f83-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f83-105">Syntax</span></span>

<span data-ttu-id="25f83-106">*expressão* . IsolateODBCTrans</span><span class="sxs-lookup"><span data-stu-id="25f83-106">*expression* .IsolateODBCTrans</span></span>

<span data-ttu-id="25f83-107">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="25f83-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f83-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="25f83-108">Remarks</span></span>

<span data-ttu-id="25f83-p101">Em algumas situações, será necessário ter várias transações simultâneas pendentes na mesma conexão ODBC. Para fazer isso, será necessário abrir um **Workspace** separado para cada transação. Embora cada **Workspace** possa ter sua própria conexão ODBC com o banco de dados, isso reduz a velocidade de desempenho do sistema. Como o isolamento da transação geralmente não é necessário, as conexões ODBC de vários objetos **Workspace** abertas pelo mesmo usuário são compartilhados por padrão.</span><span class="sxs-lookup"><span data-stu-id="25f83-p101">In some situations, you need to have multiple simultaneous transactions pending on the same ODBC connection. To do this, you need to open a separate **Workspace** for each transaction. Although each **Workspace** can have its own ODBC connection to the database, this slows system performance. Because transaction isolation isn't usually required, ODBC connections from multiple **Workspace** objects opened by the same user are shared by default.</span></span>

<span data-ttu-id="25f83-p102">Alguns servidores ODBC, como o Microsoft SQL Server, não permitem transações simultâneas em uma única conexão. Se você precisa ter mais de uma transação pendente simultânea em relação a um banco de dados, defina a propriedade **IsolateODBCTrans** como **True** em cada **Workspace** assim que abri-lo. Isso força uma conexão ODBC separada para cada **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="25f83-p102">Some ODBC servers, such as Microsoft SQL Server, don't allow simultaneous transactions on a single connection. If you need to have more than one transaction at a time pending against such a database, set the **IsolateODBCTrans** property to **True** on each **Workspace** as soon as you open it. This forces a separate ODBC connection for each **Workspace**.</span></span>

