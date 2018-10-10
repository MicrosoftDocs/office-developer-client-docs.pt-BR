---
title: Adicionando dados a um Recordset
TOCTitle: Adding Data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42cdf33d7b34dc4a48392d21dcdb2d9de26b4bbc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463463"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="793ad-102">Adicionando dados a um Recordset</span><span class="sxs-lookup"><span data-stu-id="793ad-102">Adding Data to a Recordset</span></span>


<span data-ttu-id="793ad-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="793ad-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="793ad-p101">É provável que o **Recordset** seja o objeto mais utilizado do ADO. No ADO, um **Recordset** é considerado como a combinação de um conjunto de resultados de uma fonte de dados com seus comportamentos de cursor associados. Portanto, você pode incluir dados em um **Recordset** e, em seguida, usar os métodos e as propriedades do **Recordset** para navegar pelas linhas de dados, exibir os valores das linhas e, de outro modo, manipular o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="793ad-p101">The **Recordset** is probably the most used of the ADO objects. In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors. Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="793ad-p102">Esta seção se concentrará na adição de dados ao **Recordset**. Para obter informações sobre como navegar pelos dados ou atualizá-los, consulte o [Capítulo 4: Editando dados](chapter-4-editing-data.md) e o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md). Nem sempre os recursos avançados de um objeto **Command** são necessários para adicionar o conjunto de resultados a um **Recordset**. Geralmente, você pode executar seu comando definindo a propriedade **Source** no **Recordset** ou passando um sequência de comandos ao método **Open** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="793ad-p102">This section will focus on adding data to the **Recordset**. For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md). You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**. Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="793ad-p103">Há diversas maneiras de adicionar dados da fonte de dados a um **Recordset**. A técnica usada depende das necessidades do aplicativo e dos recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="793ad-p103">There are a variety of ways to add data from your data source to a **Recordset**. The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

