---
title: Objeto de Conexão (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 73ede9cae5246db3d802125b0f7c4e6df5347930
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716786"
---
# <a name="connection-object-dao"></a><span data-ttu-id="7b0f1-102">Objeto de Conexão (DAO)</span><span class="sxs-lookup"><span data-stu-id="7b0f1-102">Connection object (DAO)</span></span>

<span data-ttu-id="7b0f1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b0f1-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="7b0f1-p101">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="7b0f1-106">Um objeto **Connection** representa uma conexão com um banco de dados ODBC (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="7b0f1-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b0f1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b0f1-107">Remarks</span></span>

<span data-ttu-id="7b0f1-p102">**Connection** é um objeto não persistente que representa uma conexão com um banco de dados remoto. O objeto **Connection** está disponível somente nos espaços de trabalho ODBCDirect (isto é, um objeto **Workspace** criado com a opção de tipo definida como **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="7b0f1-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>

> [!NOTE]
> <span data-ttu-id="7b0f1-p103">[!OBSERVAçãO] O código gravado por versões anteriores do DAO pode continuar usando o objeto **Database** para obter compatibilidade com versões anteriores, mas se os novos recursos de um objeto **Connection** forem desejados, você deverá revisar o código para usar o objeto **Connection**. Para ajudar na conversão de código, será possível obter uma referência do objeto **Connection** a partir de um **Database**, lendo a propriedade [Connection](database-connection-property-dao.md) do objeto **Database**. Por outro lado, você pode obter uma referência do objeto **Database** a partir da propriedade **Database** do objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-p103">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object. To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object. Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>


