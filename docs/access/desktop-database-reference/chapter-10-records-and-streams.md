---
title: 'Capítulo 10: Registros e fluxos'
TOCTitle: 'Chapter 10: Records and streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a47ac1f850905546651ffbdd708887bf7d74940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296490"
---
# <a name="chapter-10-records-and-streams"></a><span data-ttu-id="05827-102">Capítulo 10: Registros e fluxos</span><span class="sxs-lookup"><span data-stu-id="05827-102">Chapter 10: Records and streams</span></span>

<span data-ttu-id="05827-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05827-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05827-p101">O ADO atualmente fornece o objeto [Recordset](recordset-object-ado.md) como o principal meio de acessar informações nas fontes de dados, como bancos de dados relacionais. Entretanto, alguns provedores oferecem suporte a objetos [Record](record-object-ado.md) e [Stream](stream-object-ado.md) como objetos alternativos ou complementares com os quais os dados de provedores podem ser manipulados. Para obter especificações sobre o comportamento de **Record**, consulte a documentação do provedor.</span><span class="sxs-lookup"><span data-stu-id="05827-p101">ADO currently provides the [Recordset](recordset-object-ado.md) object as the primary means of accessing information in data sources, such as relational databases. However, some providers support the [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects as alternative or complementary objects with which data from providers can be manipulated. For specifics on **Record** behavior, see your provider's documentation.</span></span>

## <a name="records"></a><span data-ttu-id="05827-107">Registros</span><span class="sxs-lookup"><span data-stu-id="05827-107">Records</span></span>

<span data-ttu-id="05827-p102">Os objetos **Record** funcionam essencialmente como um **Recordset** de uma linha. Entretanto, **Records** têm funções limitadas em comparação ao **Recordsets** e têm diferentes propriedades e métodos. A fonte para os dados no objeto **Record** pode ser um comando que retorne uma linha de dados do provedor. A utilização de objetos **Record** em vez de objetos **Recordset** para receber os resultados de uma consulta que retorne uma linha de dados elimina a sobrecarga de instanciação de um objeto **Recordset** mais complexo.</span><span class="sxs-lookup"><span data-stu-id="05827-p102">**Record** objects essentially function as one-row **Recordset** s. However, **Records** have limited functionality compared to **Recordsets** and they have different properties and methods.The source for the data in a **Record** object can be a command which returns one row of data from the provider. Using **Record** objects rather than **Recordset** objects to receive the results from a query that returns one row of data eliminates the overhead of instantiating the more complex **Recordset** object.</span></span>

<span data-ttu-id="05827-p103">Os objetos **Record** podem servir para outro propósito, particularmente com os provedores de fontes de dados diferentes de bancos de dados relacionais tradicionais, como o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Muitas das informações que devem ser processadas existem não como tabelas nos bancos de dados, mas como mensagens em sistemas de email e como arquivos em sistemas de arquivo modernos. Os objetos **Record** e **Stream** facilitam o acesso às informações armazenadas em fontes diferentes de bancos de dados relacionais.</span><span class="sxs-lookup"><span data-stu-id="05827-p103">**Record** objects can serve another purpose, particularly with providers for data sources other than traditional relational databases, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Much of the information that must be processed exists, not as tables in databases, but as messages in electronic mail systems and files in modern file systems. The **Record** and **Stream** objects facilitate access to information stored in sources other than relational databases.</span></span>

<span data-ttu-id="05827-114">O **objeto Record** pode representar e gerenciar dados como diretórios e arquivos em um sistema de arquivos ou pastas e mensagens em um sistema de email.</span><span class="sxs-lookup"><span data-stu-id="05827-114">The **Record** object can represent and manage data such as directories and files in a file system or folders and messages in an email system.</span></span> <span data-ttu-id="05827-115">Para esses propósitos, a fonte para **Record** pode ser a linha atual de um **Recordset** aberto, uma URL absoluta ou uma URL relativa em conjunto com um objeto [Connection](connection-object-ado.md) aberto.</span><span class="sxs-lookup"><span data-stu-id="05827-115">For these purposes, the source for the **Record** can be the current row of an open **Recordset**, an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="05827-p105">Normalmente, um **Recordset** pode ser utilizado para representar um contêiner ou um pai na hierarquia, como uma pasta ou diretório. Um **Record** pode ser usado para retornar informações específicas sobre um nó no contêiner pai, como um arquivo ou documento. A principal razão para que os **Records** sejam utilizados para representar esse tipo de informação é que essas fontes de dados são heterogêneas. Isso significa que cada **Record** pode ter um conjunto e um número diferente de campos. Os **Recordsets** tradicionais que contêm linhas de um banco de dados são homogêneos, o que significa que cada linha tem o mesmo número e tipo de campos.</span><span class="sxs-lookup"><span data-stu-id="05827-p105">Typically, a **Recordset** can be used to represent a container or parent in a hierarchy such as a folder or directory. A **Record** can be used to return specific information about one node in the parent container, such as a file or document. The primary reason **Records** are used to represent this type of information is that these sources of data are heterogenous. This means that each **Record** may have a different set and number of fields. Traditional **Recordsets** containing rows from a database are homogenous, which means that each row has the same number and type of fields.</span></span>

<span data-ttu-id="05827-121">Para obter mais informações sobre a utilização do objeto **Record** para o processamento desses dados heterogêneos do provedor, como o Internet Publishing Provider, consulte [Usando o ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="05827-121">For more information about using the **Record** object for processing this heterogeneous data from providers such as the Internet Publishing Provider, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

## <a name="streams"></a><span data-ttu-id="05827-122">Streams</span><span class="sxs-lookup"><span data-stu-id="05827-122">Streams</span></span>

<span data-ttu-id="05827-p106">O objeto **Stream** fornece os meios para ler, escrever e gerenciar um fluxo de bytes. Esse fluxo de bytes pode ser texto ou um binário e está limitado em tamanho apenas por recursos de sistema. Em geral, os objetos **Stream** do ADO são utilizados com os seguintes propósitos:</span><span class="sxs-lookup"><span data-stu-id="05827-p106">The **Stream** object provides the means to read, write, and manage a stream of bytes. This byte stream may be text or binary and is limited in size only by system resources. Typically, ADO **Stream** objects are used for the following purposes:</span></span>

- <span data-ttu-id="05827-p107">Para conter o texto ou os bytes que compõem um arquivo ou uma mensagem, normalmente usado com provedores como o Microsoft OLE DB Provider for Internet Publishing. Para obter mais informações sobre esse uso dos objetos **Stream**, consulte [Usando o ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="05827-p107">To contain the text or bytes that comprise a file or message, typically used with providers such as the Microsoft OLE DB Provider for Internet Publishing. For more information about this use of **Stream** objects, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

<span data-ttu-id="05827-128">Um objeto **Stream** pode ser aberto em:</span><span class="sxs-lookup"><span data-stu-id="05827-128">A **Stream** object can be opened on:</span></span>

- <span data-ttu-id="05827-129">Um arquivo simples especificado como uma URL.</span><span class="sxs-lookup"><span data-stu-id="05827-129">A simple file specified with a URL.</span></span>

- <span data-ttu-id="05827-130">Um campo de um **Record** ou um **Recordset** contendo um objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="05827-130">A field of a **Record** or **Recordset** containing a **Stream** object.</span></span>

- <span data-ttu-id="05827-131">Um fluxo padrão de um objeto **Record** ou **Recordset** representando um diretório ou arquivo composto.</span><span class="sxs-lookup"><span data-stu-id="05827-131">The default stream of a **Record** or **Recordset** object representing a directory or compound file.</span></span>

- <span data-ttu-id="05827-132">Um campo de recursos contendo a URL de um arquivo simples.</span><span class="sxs-lookup"><span data-stu-id="05827-132">A resource field containing the URL of a simple file.</span></span>

- <span data-ttu-id="05827-p108">Nenhuma fonte em particular. Nesse caso, um objeto **Stream** é aberto na memória. Os dados podem ser escritos nele e salvos em outros **Stream** ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="05827-p108">No particular source at all. In this case, a **Stream** object is opened in memory. Data can be written to it and then saved in another **Stream** or file.</span></span>

- <span data-ttu-id="05827-136">Um campo BLOB em um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="05827-136">A BLOB field in a **Recordset**.</span></span>

<span data-ttu-id="05827-137">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="05827-137">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="05827-138">Fluxos e persistência</span><span class="sxs-lookup"><span data-stu-id="05827-138">Streams and persistence</span></span>](streams-and-persistence.md)
- [<span data-ttu-id="05827-139">Campos fornecidos pelo provedor e registros</span><span class="sxs-lookup"><span data-stu-id="05827-139">Records and provider-supplied fields</span></span>](records-and-provider-supplied-fields.md)
- [<span data-ttu-id="05827-140">URLs absolutas e relativas</span><span class="sxs-lookup"><span data-stu-id="05827-140">Absolute and relative URLs</span></span>](absolute-and-relative-urls.md)
- [<span data-ttu-id="05827-141">Usando o ADO para publicação na Internet (ADO)</span><span class="sxs-lookup"><span data-stu-id="05827-141">Using ADO for Internet publishing (ADO)</span></span>](using-ado-for-internet-publishing.md)
