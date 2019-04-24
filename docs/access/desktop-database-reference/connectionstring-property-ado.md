---
title: Propriedade ConnectionString (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295706"
---
# <a name="connectionstring-property-ado"></a><span data-ttu-id="7e72b-102">Propriedade ConnectionString (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e72b-102">ConnectionString property (ADO)</span></span>


<span data-ttu-id="7e72b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e72b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e72b-104">Indica as informações usadas para estabelecer uma conexão com uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7e72b-104">Indicates the information used to establish a connection to a data source.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7e72b-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7e72b-105">Settings and return values</span></span>

<span data-ttu-id="7e72b-106">Define ou retorna um valor **String**.</span><span class="sxs-lookup"><span data-stu-id="7e72b-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e72b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e72b-107">Remarks</span></span>

<span data-ttu-id="7e72b-108">Use a propriedade **ConnectionString** para especificar uma fonte de dados passando uma sequência de caracteres de conexão detalhada contendo uma série de instruções *Argument* *= Value* separadas por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="7e72b-108">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="7e72b-p101">O ADO oferece suporte a cinco argumentos para a propriedade **ConnectionString**; quaisquer outros argumentos são passados diretamente para o provedorsem serem processados pelo ADO. Os argumentos aos quais o ADO oferece suporte são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="7e72b-p101">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO. The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e72b-111">Argument</span><span class="sxs-lookup"><span data-stu-id="7e72b-111">Argument</span></span></p></th>
<th><p><span data-ttu-id="7e72b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e72b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e72b-113"><em>Provedor =</em></span><span class="sxs-lookup"><span data-stu-id="7e72b-113"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="7e72b-114">Especifica o nome de um provedor a ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="7e72b-114">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e72b-115"><em>File Name=</em></span><span class="sxs-lookup"><span data-stu-id="7e72b-115"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="7e72b-116">Especifica o nome de um arquivo específico do provedor (por exemplo, um objeto de fonte de dados persistente) contendo informações de conexão predefinidas.</span><span class="sxs-lookup"><span data-stu-id="7e72b-116">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e72b-117"><em>Remote Provider=</em></span><span class="sxs-lookup"><span data-stu-id="7e72b-117"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="7e72b-118">Especifica o nome do provedor a ser usado durante a abertura de uma conexão no cliente.</span><span class="sxs-lookup"><span data-stu-id="7e72b-118">Specifies the name of a provider to use when opening a client-side connection.</span></span> <span data-ttu-id="7e72b-119">(Apenas para o Remote Data Service.)</span><span class="sxs-lookup"><span data-stu-id="7e72b-119">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e72b-120"><em>Remote Server=</em></span><span class="sxs-lookup"><span data-stu-id="7e72b-120"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="7e72b-121">Especifica o nome do caminho do servidor a ser usado ao abrir uma conexão do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="7e72b-121">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="7e72b-122">(Apenas para o Remote Data Service.)</span><span class="sxs-lookup"><span data-stu-id="7e72b-122">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e72b-123"><em>URL =</em></span><span class="sxs-lookup"><span data-stu-id="7e72b-123"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="7e72b-124">Especifica a cadeia de caracteres de conexão como uma URL absoluta que identifica um recurso, como um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="7e72b-124">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e72b-125">Depois que a propriedade **ConnectionString** for definida e o objeto [Connection](connection-object-ado.md) aberto, o provedor poderá alterar o conteúdo da propriedade, por exemplo, mapeando os nomes de argumento definidos pelo ADO para os seus equivalentes no provedor.</span><span class="sxs-lookup"><span data-stu-id="7e72b-125">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="7e72b-126">A propriedade **ConnectionString** herda automaticamente o valor usado para o argumento *ConnectionString* do método [Open](open-method-ado-connection.md), de modo que você possa substituir a propriedade **ConnectionString** atual durante a chamada do método **Open**.</span><span class="sxs-lookup"><span data-stu-id="7e72b-126">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="7e72b-127">Como o argumento *File Name* faz com que o ADO carregue o provedor associado, não é possível passar ambos os argumentos, *Provider* e *File Name*.</span><span class="sxs-lookup"><span data-stu-id="7e72b-127">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="7e72b-128">A propriedade **ConnectionString** será leitura/gravação quando a conexão estiver fechada e somente leitura quando estiver aberta.</span><span class="sxs-lookup"><span data-stu-id="7e72b-128">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="7e72b-p104">As duplicatas de um argumento na propriedade **ConnectionString** serão ignoradas. A última instância do argumento será usada.</span><span class="sxs-lookup"><span data-stu-id="7e72b-p104">Duplicates of an argument in the **ConnectionString** property are ignored. The last instance of any argument is used.</span></span>

<span data-ttu-id="7e72b-131">**Uso do Remote Data Service** Quando usado em um objeto **Connection** do lado do cliente, a propriedade **ConnectionString** pode incluir apenas os parâmetros *Remote Provider* e *Remote Server* .</span><span class="sxs-lookup"><span data-stu-id="7e72b-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

