---
title: Modelo de programação do RDS básico
TOCTitle: Basic RDS Programming Model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a90423f6bd05ae3d721faf97291ea6d21aa4393
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463878"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="341dc-102">Modelo de programação do RDS básico</span><span class="sxs-lookup"><span data-stu-id="341dc-102">Basic RDS Programming Model</span></span>


<span data-ttu-id="341dc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="341dc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="341dc-p101">O RDS lida com aplicativos existentes no seguinte ambiente: um aplicativo cliente especifica um programa a ser executado em um servidor e os parâmetros necessários para retornar as informações desejadas. O programa invocado no servidor obtém acesso à fonte de dados especificada, recupera as informações, talvez processe os dados e retorna as informações resultantes para o aplicativo cliente de modo que elas possam ser facilmente utilizadas. O RDS fornece os meios para realizar a seguinte sequência de ações:</span><span class="sxs-lookup"><span data-stu-id="341dc-p101">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information. The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use. RDS provides the means for you to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="341dc-p102">Especificar o programa a ser invocado no servidor e obter um modo de referir-se a ele a partir do cliente. (Essa referência é chamada, às vezes, de  *proxy*. Ela representa o programa do servidor remoto. O aplicativo cliente "chamará" o proxy como se fosse um programa local, mas, na verdade, ele invocará o programa do servidor remoto.)</span><span class="sxs-lookup"><span data-stu-id="341dc-p102">Specify the program to be invoked on the server, and obtain a way to refer to it from the client. (This reference is sometimes called a *proxy*. It represents the remote server program. The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

  - <span data-ttu-id="341dc-p103">Invocar o programa do servidor. Passar parâmetros ao programa do servidor que identifiquem a fonte de dados e o comando a ser lançado. (O programa do servidor usa o ADO para obter o acesso à fonte de dados. O ADO faz a conexão com um dos parâmetros fornecidos e depois lança o comando especificado em outro parâmetro.)</span><span class="sxs-lookup"><span data-stu-id="341dc-p103">Invoke the server program. Pass parameters to the server program that identify the data source and the command to issue. (The server program actually uses ADO to gain access to the data source. ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

  - <span data-ttu-id="341dc-p104">O programa do servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados. Opcionalmente, o objeto **Recordset** é processado no servidor.</span><span class="sxs-lookup"><span data-stu-id="341dc-p104">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source. Optionally, the **Recordset** object is processed on the server.</span></span>

  - <span data-ttu-id="341dc-117">O programa do servidor retorna o objeto **Recordset** final para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="341dc-117">The server program returns the final **Recordset** object to the client application.</span></span>

  - <span data-ttu-id="341dc-118">No cliente, o objeto **Recordset** é colocado em um formato no qual ela possa ser facilmente utilizado por controles visuais.</span><span class="sxs-lookup"><span data-stu-id="341dc-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

  - <span data-ttu-id="341dc-119">Quaisquer modificações no objeto **Recordset** são retornadas para o programa do servidor que as usa para atualizar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="341dc-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="341dc-p105">Esse modelo de programação contém determinados recursos de conveniência. Se você não precisar de um programa de servidor complexo para acessar a fonte de dados e fornecer os parâmetros de conexão e comando necessários, o RDS recuperará automaticamente os dados especificados com um programa de servidor padrão simples.</span><span class="sxs-lookup"><span data-stu-id="341dc-p105">This programming model contains certain convenience features. If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="341dc-p106">Se precisar de processamento mais complexo, você poderá especificar seu próprio programa de servidor personalizado. Por exemplo, como um programa de servidor tem todo o poder do ADO à sua disposição, ele poderia conectar-se a diversas fontes de dados diferentes, combinar seus dados de um modo complexo e, depois, retornar um resultado processado simples para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="341dc-p106">If you need more complex processing, you can specify your own custom server program. For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="341dc-124">Finalmente, se suas necessidades estiverem no meio do caminho, o ADO agora oferece suporte à personalização do comportamento do programa de servidor padrão.</span><span class="sxs-lookup"><span data-stu-id="341dc-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>

