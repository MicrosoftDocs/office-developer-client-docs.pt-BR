---
title: 'Apêndice A: provedores'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbd9536edd15f923af85f2fadad8b696077af4a4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464489"
---
# <a name="appendix-a-providers"></a><span data-ttu-id="37f17-102">Apêndice A: provedores</span><span class="sxs-lookup"><span data-stu-id="37f17-102">Appendix A: Providers</span></span>


<span data-ttu-id="37f17-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37f17-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="37f17-p101">Esta seção descreve três tipos de provedores: provedores de dados, provedores de serviços e componentes de serviço. Os provedores enquadram-se em duas categorias: os que fornecem dados e os que fornecem serviços. Um *provedor de dados* possui seus próprios dados e os exibe em um formulário tabular para seu aplicativo. Um *provedor de serviços* encapsula um serviço gerando e consumindo dados, aumentando recursos em aplicativos do ADO. Um provedor de serviços também pode ser definido posteriormente como um *componente de serviço*, que deverá trabalhar juntamente com outros provedores ou componentes de serviços.</span><span class="sxs-lookup"><span data-stu-id="37f17-p101">This section addresses three kinds of providers: data providers, service providers, and service components. Providers fall into two categories: those providing data and those providing services. A *data provider* owns its own data and exposes it in tabular form to your application. A *service provider* encapsulates a service by producing and consuming data, augmenting features in your ADO applications. A service provider may also be further defined as a *service component*, which must work in conjunction with other service providers or components.</span></span>

## <a name="data-providers"></a><span data-ttu-id="37f17-109">Provedores de dados</span><span class="sxs-lookup"><span data-stu-id="37f17-109">Data Providers</span></span>

<span data-ttu-id="37f17-110">O ADO é poderoso e flexível, pois pode conectar-se a qualquer um dos vários provedores de dados e ainda apresentar o mesmo modelo de programação, independentemente dos recursos específicos de um determinado provedor.</span><span class="sxs-lookup"><span data-stu-id="37f17-110">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span>

<span data-ttu-id="37f17-p102">Entretanto, pelo fato de cada provedor de dados ser exclusivo, a forma de seu aplicativo interagir com o ADO variará ligeiramente de acordo com o provedor de dados. As diferenças geralmente enquadram-se em três categorias:</span><span class="sxs-lookup"><span data-stu-id="37f17-p102">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider. The differences usually fall into one of three categories:</span></span>

  - <span data-ttu-id="37f17-113">Parâmetros de conexão na propriedade [ConnectionString](connectionstring-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37f17-113">Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

  - <span data-ttu-id="37f17-114">Uso do objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37f17-114">[Command](command-object-ado.md) object usage.</span></span>

  - <span data-ttu-id="37f17-115">Comportamento específico do provedor [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37f17-115">Provider-specific [Recordset](recordset-object-ado.md) behavior.</span></span>

<span data-ttu-id="37f17-116">Os detalhes de cada um dos provedores de dados atualmente disponíveis na Microsoft estão relacionados a seguir.</span><span class="sxs-lookup"><span data-stu-id="37f17-116">Details for each of the data providers currently available from Microsoft are listed as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37f17-117">Área</span><span class="sxs-lookup"><span data-stu-id="37f17-117">Area</span></span></p></th>
<th><p><span data-ttu-id="37f17-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="37f17-118">Topic</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37f17-119">Bancos de dados ODBC</span><span class="sxs-lookup"><span data-stu-id="37f17-119">ODBC databases</span></span></p></td>
<td><p><span data-ttu-id="37f17-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span><span class="sxs-lookup"><span data-stu-id="37f17-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37f17-121">Serviço de Indexação da Microsoft</span><span class="sxs-lookup"><span data-stu-id="37f17-121">Microsoft Indexing Service</span></span></p></td>
<td><p><span data-ttu-id="37f17-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span><span class="sxs-lookup"><span data-stu-id="37f17-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37f17-123">Serviço do Active Directory da Microsoft</span><span class="sxs-lookup"><span data-stu-id="37f17-123">Microsoft Active Directory Service</span></span></p></td>
<td><p><span data-ttu-id="37f17-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span><span class="sxs-lookup"><span data-stu-id="37f17-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37f17-125">Bancos de dados do Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="37f17-125">Microsoft Jet databases</span></span></p></td>
<td><p><span data-ttu-id="37f17-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">OLE DB Provider for Microsoft Jet</a></span><span class="sxs-lookup"><span data-stu-id="37f17-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">OLE DB Provider for Microsoft Jet</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37f17-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="37f17-127">Microsoft SQL Server</span></span></p></td>
<td><p><span data-ttu-id="37f17-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span><span class="sxs-lookup"><span data-stu-id="37f17-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37f17-129">Bancos de dados Oracle</span><span class="sxs-lookup"><span data-stu-id="37f17-129">Oracle databases</span></span></p></td>
<td><p><span data-ttu-id="37f17-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span><span class="sxs-lookup"><span data-stu-id="37f17-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37f17-131">Publicação na Internet</span><span class="sxs-lookup"><span data-stu-id="37f17-131">Internet Publishing</span></span></p></td>
<td><p><span data-ttu-id="37f17-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span><span class="sxs-lookup"><span data-stu-id="37f17-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a><span data-ttu-id="37f17-133">Propriedades dinâmicas específicas para o provedor</span><span class="sxs-lookup"><span data-stu-id="37f17-133">Provider-Specific Dynamic Properties</span></span>

<span data-ttu-id="37f17-p103">A coleção [Properties](properties-collection-ado.md) dos objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) e [Recordset](recordset-object-ado.md) incluem propriedades dinâmicasespecíficas para o provedor. Essas propriedades fornecem informações sobre a funcionalidade específica do provedor, além das propriedades internas que têm suporte do ADO.</span><span class="sxs-lookup"><span data-stu-id="37f17-p103">The [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), and [Recordset](recordset-object-ado.md) objects include dynamic properties specific to the provider. These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</span></span>

<span data-ttu-id="37f17-p104">Depois de estabelecer a conexão e criar esses objetos, utilize o método [Refresh](refresh-method-ado.md) na coleção **Properties** do objeto para obter as propriedades específicas para o provedor. Consulte a documentação do provedor e a Referência do programador do OLE DB para obter informações detalhadas sobre essas propriedades dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="37f17-p104">After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties. Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.</span></span>

## <a name="service-providers"></a><span data-ttu-id="37f17-138">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="37f17-138">Service Providers</span></span>

<span data-ttu-id="37f17-p105">Para utilizar um provedor de serviços, você deverá fornecer uma palavra-chave. Também deverá conhecer as propriedades dinâmicas específicas para o provedor associadas a cada provedor de serviços. Os detalhes específicos para provedor são relacionados para cada um dos provedores de serviços atualmente disponíveis na Microsoft:</span><span class="sxs-lookup"><span data-stu-id="37f17-p105">To use a service provider, you must supply a keyword. You should also be aware of the provider-specific dynamic properties associated with each service provider. Provider-specific details are listed for each of the service providers currently available from Microsoft:</span></span>

  - [<span data-ttu-id="37f17-142">Microsoft Data Shaping Service para OLE DB</span><span class="sxs-lookup"><span data-stu-id="37f17-142">Microsoft Data Shaping Service for OLE DB</span></span>](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

  - [<span data-ttu-id="37f17-143">Microsoft OLE DB Persistence Provider</span><span class="sxs-lookup"><span data-stu-id="37f17-143">Microsoft OLE DB Persistence Provider</span></span>](microsoft-ole-db-persistence-provider-ado-service-provider.md)

  - [<span data-ttu-id="37f17-144">Microsoft OLE DB Remoting Provider</span><span class="sxs-lookup"><span data-stu-id="37f17-144">Microsoft OLE DB Remoting Provider</span></span>](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a><span data-ttu-id="37f17-145">Componentes de serviço</span><span class="sxs-lookup"><span data-stu-id="37f17-145">Service Components</span></span>

<span data-ttu-id="37f17-p106">O componente de serviço [Cursor Service para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) complementa as funções de suporte do cursor dos provedores de dados. Também exige uma palavra-chave e tem propriedades dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="37f17-p106">The [Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) service component supplements the cursor support functions of data providers. It also requires a keyword and has dynamic properties.</span></span>

<span data-ttu-id="37f17-148">Para obter mais informações sobre provedores, consulte a documentação do Microsoft OLE DB no Microsoft Data Access Components SDK ou visite o site [Centro do Desenvolverdo da Plataforma de Dados](https://msdn.microsoft.com/data/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="37f17-148">For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://msdn.microsoft.com/data/default.aspx).</span></span>

## <a name="provider-commands"></a><span data-ttu-id="37f17-149">Comandos do provedor</span><span class="sxs-lookup"><span data-stu-id="37f17-149">Provider Commands</span></span>

<span data-ttu-id="37f17-150">Para cada provedor listado aqui, se seus aplicativos permitir que os usuários insiram as instruções SQL que os comandos do provedor, você deve sempre validar a entrada do usuário e ser cuidadoso de phishing possíveis usando a instrução SQL potencialmente perigosa, como, como parte do entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="37f17-150">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statement, such as, , as part of the user input.</span></span>

