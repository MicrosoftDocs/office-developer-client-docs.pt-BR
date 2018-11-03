---
title: Programação ADO/WFC
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58ec04f92bf4d1eaaa8ea36c5937cae0bab3729f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943819"
---
# <a name="adowfc-programming"></a><span data-ttu-id="0c29c-102">Programação ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0c29c-102">ADO/WFC programming</span></span>

<span data-ttu-id="0c29c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c29c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c29c-p101">Para o Microsoft Visual J++ 6.0, o ADO foi estendido para trabalhar com o WFC (Windows Foundation Classes) das seguintes maneiras. Primeiramente, um conjunto de classes Java foi implementado estendendo as interfaces ADO e criando notificações de interesse ao programador Java; as classes Java também expõem funções que retornam tipos Java ao usuário. Para aprimorar o desempenho, a classe Java acessa diretamente os tipos de dados nativos no objeto do conjunto de linhas OLE DB e os retorna ao programador Java como tipos Java sem convertê-los primeiro de e para uma variante. O ADO também foi estendido pra trabalhar com notificações de eventos na estrutura WFC.</span><span class="sxs-lookup"><span data-stu-id="0c29c-p101">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways. First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user. To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant. ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="0c29c-p102">O ADO para Windows Foundation Classes (ADO/WFC) suporta todos os métodos, propriedades, objetos e eventos do ADO padrão. No entanto, as operações que requerem uma variante como um parâmetro e mostram excelente desempenho em uma linguagem como Microsoft Visual Basic, exibem menos desempenho em uma linguagem como Visual J++. Por esse motivo, o ADO/WFC também fornece funções de acesso no objeto [Field](field-object-ado.md) que assume tipos de dados Java nativos em vez do tipo de dados da variante.</span><span class="sxs-lookup"><span data-stu-id="0c29c-p102">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events. However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++. For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="0c29c-111">Para obter informações mais detalhadas dentro da documentação ADO sobre os pacotes ADO/WFC, consulte o [ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0c29c-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="0c29c-112">Fazendo referência à biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c29c-112">Referencing the library</span></span>

<span data-ttu-id="0c29c-113">Para importar as classes de dados ADO/WFC em seu projeto, inclua a seguinte linha em seu código:</span><span class="sxs-lookup"><span data-stu-id="0c29c-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

