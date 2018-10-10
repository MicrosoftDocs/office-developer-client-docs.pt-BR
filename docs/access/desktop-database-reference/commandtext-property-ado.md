---
title: Propriedade CommandText (ADO)
TOCTitle: CommandText Property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9000f069c7669872c686c013520f886d16e3619b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462012"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="a7a4e-102">Propriedade CommandText (ADO)</span><span class="sxs-lookup"><span data-stu-id="a7a4e-102">CommandText Property (ADO)</span></span>


<span data-ttu-id="a7a4e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7a4e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a7a4e-104">Indica o texto de um comando a ser emitido para um provedor.</span><span class="sxs-lookup"><span data-stu-id="a7a4e-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a7a4e-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a7a4e-105">Settings and Return Values</span></span>

<span data-ttu-id="a7a4e-p101">Define ou retorna um valor **String** contendo um comando de provedor, como uma instrução SQL, um nome de tabela, uma URL relativa ou uma chamada de procedimento armazenado. O padrão é "" (sequência de comprimento zero).</span><span class="sxs-lookup"><span data-stu-id="a7a4e-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7a4e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7a4e-108">Remarks</span></span>

<span data-ttu-id="a7a4e-p102">Use a propriedade **CommandText** para definir ou retornar o texto de um comando representado por um objeto [Command](command-object-ado.md). Geralmente, é uma instrução SQL, mas também pode ser qualquer outro tipo de instrução de comando reconhecida pelo provedor, como uma chamada de procedimento armazenado. Uma instrução SQL deve ser de um dialeto ou versão específica que tenha suporte do processador de consultas do provedor.</span><span class="sxs-lookup"><span data-stu-id="a7a4e-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="a7a4e-112">Se a propriedade [Prepared](prepared-property-ado.md) do objeto **Command** estiver definida como **True** e o objeto **Command** estiver vinculado a uma conexão aberta quando você definir a propriedade **CommandText**, o ADO preparará a consulta (isto é, um formulário compilado da consulta que é armazenado pelo provedor) quando você chamar os métodos [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) ou **Open**.</span><span class="sxs-lookup"><span data-stu-id="a7a4e-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) or **Open** methods.</span></span>

<span data-ttu-id="a7a4e-p103">Dependendo da definição da propriedade [CommandType](commandtype-property-ado.md), o ADO poderá alterar a propriedade **CommandText**. Você pode ler a propriedade **CommandText** a qualquer momento para ver o texto de comando real que será utilizado pelo ADO durante a execução.</span><span class="sxs-lookup"><span data-stu-id="a7a4e-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="a7a4e-p104">Use a propriedade **CommandText** para definir ou retornar uma URL relativa que especifique um recurso, como um arquivo ou um diretório. O recurso é relativo a um local especificado explicitamente por uma URL absoluta ou implicitamente por um objeto [Connection](connection-object-ado.md) aberto.</span><span class="sxs-lookup"><span data-stu-id="a7a4e-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a7a4e-p105">[!OBSERVAçãO] As URLs que usam o esquema http invocarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs absolutas e relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="a7a4e-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


