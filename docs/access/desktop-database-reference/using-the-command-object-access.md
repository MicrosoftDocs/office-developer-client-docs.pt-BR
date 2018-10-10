---
title: Usando o objeto Command (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462427"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="2a379-102">Usando o objeto Command (Access)</span><span class="sxs-lookup"><span data-stu-id="2a379-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="2a379-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a379-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a379-p101">Depois de se conectar a uma fonte de dados, você precisa executar as solicitações nela para obter os conjuntos de resultados. O ADO encapsula este tipo de funcionalidade de comando no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="2a379-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="2a379-p102">Você pode usar o objeto **Command** para solicitar qualquer tipo de operação do provedor, considerando que o provedor pode interpretar a sequência do comando adequadamente. Uma operação comum para os provedores de dados é consultar um banco de dados e retornar os registros em um objeto **Recordset**. **Recordset**s serão abordados posteriormente neste e em outros capítulos; por enquanto, considere-os como ferramentas para manter e visualizar os conjuntos de resultados. Como com muitos objetos ADO, dependendo da funcionalidade do provedor, algumas propriedades, métodos e coleções do objeto **Command** podem gerar erros quando mencionados.</span><span class="sxs-lookup"><span data-stu-id="2a379-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="2a379-p103">Nem sempre é necessário criar um objeto **Command** para executar um comando em uma fonte de dados. Você pode usar o método **Execute** no objeto **Connection** ou o método **Open** no objeto **Recordset**. Contudo, você deveria usar um objeto **Command** se precisar usar novamente um comando em seu código ou se precisar transmitir informações detalhadas sobre o parâmetro com seu comando. Esses cenários são abordados em detalhes posteriormente neste capítulo.</span><span class="sxs-lookup"><span data-stu-id="2a379-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2a379-p104">Determinados <STRONG>Command</STRONG>s podem retornar um resultado como um fluxo binário ou como um único <STRONG>Record</STRONG> em vez de um <STRONG>Recordset</STRONG> se houver suporte para isso pelo provedor. Além disso, alguns <STRONG>Command</STRONG>s não são destinados a retornar qualquer conjunto de resultados (por exemplo, uma consulta SQL Update). Este capítulo abordará o cenário mais comum, contudo executando <STRONG>Command</STRONG>s que retornam resultados em um objeto <STRONG>Recordset</STRONG>. Para obter mais informações sobre o retorno de resultados em  <STRONG>Record</STRONG>s ou <STRONG>Stream</STRONG>s, consulte <A href="chapter-10-records-and-streams.md">Capítulo 10: Records e Streams</A>.</span><span class="sxs-lookup"><span data-stu-id="2a379-p104">Certain <STRONG>Command</STRONG>s can return a result set as a binary stream or as a single <STRONG>Record</STRONG> rather than as a <STRONG>Recordset</STRONG>, if this is supported by the provider. Also, some <STRONG>Command</STRONG>s are not intended to return any result set at all (for example, a SQL Update query). This chapter will cover the most typical scenario, however: executing <STRONG>Command</STRONG>s that return results into a <STRONG>Recordset</STRONG> object. For more information about returning results into <STRONG>Record</STRONG>s or <STRONG>Stream</STRONG>s, see <A href="chapter-10-records-and-streams.md">Chapter 10: Records and Streams</A>.</span></span></P>


