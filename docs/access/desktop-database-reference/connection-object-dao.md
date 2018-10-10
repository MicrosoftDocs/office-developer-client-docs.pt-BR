---
title: Objeto de Conexão (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462765"
---
# <a name="connection-object-dao"></a><span data-ttu-id="2ac1f-102">Objeto de Conexão (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ac1f-102">Connection Object (DAO)</span></span>


<span data-ttu-id="2ac1f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ac1f-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="2ac1f-p101">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2ac1f-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>



<span data-ttu-id="2ac1f-106">Um objeto **Connection** representa uma conexão com um banco de dados ODBC (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="2ac1f-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ac1f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ac1f-107">Remarks</span></span>

<span data-ttu-id="2ac1f-p102">**Connection** é um objeto não persistente que representa uma conexão com um banco de dados remoto. O objeto **Connection** está disponível somente nos espaços de trabalho ODBCDirect (isto é, um objeto **Workspace** criado com a opção de tipo definida como **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="2ac1f-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="2ac1f-p103">[!OBSERVAçãO] O código gravado por versões anteriores do DAO pode continuar usando o objeto <STRONG>Database</STRONG> para obter compatibilidade com versões anteriores, mas se os novos recursos de um objeto <STRONG>Connection</STRONG> forem desejados, você deverá revisar o código para usar o objeto <STRONG>Connection</STRONG>. Para ajudar na conversão de código, será possível obter uma referência do objeto <STRONG>Connection</STRONG> a partir de um <STRONG>Database</STRONG>, lendo a propriedade <A href="database-connection-property-dao.md">Connection</A> do objeto <STRONG>Database</STRONG>. Por outro lado, você pode obter uma referência do objeto <STRONG>Database</STRONG> a partir da propriedade <STRONG>Database</STRONG> do objeto <STRONG>Connection</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2ac1f-p103">Code written for earlier versions of DAO can continue to use the <STRONG>Database</STRONG> object for backward compatibility, but if the new features of a <STRONG>Connection</STRONG> are desired, you should revise code to use the <STRONG>Connection</STRONG> object. To help with code conversion, you can obtain a <STRONG>Connection</STRONG> object reference from a <STRONG>Database</STRONG> by reading the <A href="database-connection-property-dao.md">Connection</A> property of the <STRONG>Database</STRONG> object. Conversely, you can obtain a <STRONG>Database</STRONG> object reference from the <STRONG>Connection</STRONG> object's <STRONG>Database</STRONG> property.</span></span></P>


