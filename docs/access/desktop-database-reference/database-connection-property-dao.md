---
title: Propriedade Database.Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d000d2f01bea7746fb249ab7f9acacc047029b21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463059"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="e75bf-102">Propriedade Database.Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="e75bf-102">Database.Connection Property (DAO)</span></span>


<span data-ttu-id="e75bf-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e75bf-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="e75bf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e75bf-104">Syntax</span></span>

<span data-ttu-id="e75bf-105">*expressão* . Conexão</span><span class="sxs-lookup"><span data-stu-id="e75bf-105">*expression* .Connection</span></span>

<span data-ttu-id="e75bf-106">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="e75bf-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e75bf-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e75bf-107">Remarks</span></span>

<span data-ttu-id="e75bf-p101">Use a propriedade **Connection** para obter uma referência a um objeto **Connection** que corresponda ao **Database**. No DAO, um objeto **Connection** e seus objetos **Database** correspondentes são simplesmente duas referências diferentes de variáveis de objeto para o mesmo objeto. A propriedade **[Database](connection-database-property-dao.md)** de um objeto **Connection** e a propriedade **Connection** de um objeto **Database** facilita a alteração das conexões para uma fonte de dados ODBC por meio do mecanismo de banco de dados do Microsoft Access a fim de usar o ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="e75bf-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

