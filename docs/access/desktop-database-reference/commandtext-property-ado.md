---
title: Propriedade CommandText (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 66797accb24cead7d7ba5732f0a9c58ee31049e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296133"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="8d678-102">Propriedade CommandText (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d678-102">CommandText property (ADO)</span></span>


<span data-ttu-id="8d678-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d678-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d678-104">Indica o texto de um comando a ser emitido para um provedor.</span><span class="sxs-lookup"><span data-stu-id="8d678-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8d678-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8d678-105">Settings and return values</span></span>

<span data-ttu-id="8d678-p101">Define ou retorna um valor **String** contendo um comando de provedor, como uma instrução SQL, um nome de tabela, uma URL relativa ou uma chamada de procedimento armazenado. O padrão é "" (sequência de comprimento zero).</span><span class="sxs-lookup"><span data-stu-id="8d678-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d678-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d678-108">Remarks</span></span>

<span data-ttu-id="8d678-p102">Use a propriedade **CommandText** para definir ou retornar o texto de um comando representado por um objeto [Command](command-object-ado.md). Geralmente, é uma instrução SQL, mas também pode ser qualquer outro tipo de instrução de comando reconhecida pelo provedor, como uma chamada de procedimento armazenado. Uma instrução SQL deve ser de um dialeto ou versão específica que tenha suporte do processador de consultas do provedor.</span><span class="sxs-lookup"><span data-stu-id="8d678-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="8d678-112">Se a propriedade [Prepared](prepared-property-ado.md) do objeto **Command** estiver definida como **True** e o objeto **Command** estiver vinculado a uma conexão aberta quando você definir a propriedade **CommandText**, o ADO preparará a consulta (isto é, um formulário compilado da consulta que é armazenado pelo provedor) quando você chamar os métodos [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) ou **Open**.</span><span class="sxs-lookup"><span data-stu-id="8d678-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) or **Open** methods.</span></span>

<span data-ttu-id="8d678-p103">Dependendo da definição da propriedade [CommandType](commandtype-property-ado.md), o ADO poderá alterar a propriedade **CommandText**. Você pode ler a propriedade **CommandText** a qualquer momento para ver o texto de comando real que será utilizado pelo ADO durante a execução.</span><span class="sxs-lookup"><span data-stu-id="8d678-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="8d678-p104">Use a propriedade **CommandText** para definir ou retornar uma URL relativa que especifique um recurso, como um arquivo ou um diretório. O recurso é relativo a um local especificado explicitamente por uma URL absoluta ou implicitamente por um objeto [Connection](connection-object-ado.md) aberto.</span><span class="sxs-lookup"><span data-stu-id="8d678-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <span data-ttu-id="8d678-117">[!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="8d678-117">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="8d678-118">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="8d678-118">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


