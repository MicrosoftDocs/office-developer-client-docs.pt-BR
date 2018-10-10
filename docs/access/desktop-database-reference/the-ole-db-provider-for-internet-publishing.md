---
title: O OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9f8fbed638c07e55b3ecb1730633dceee2b5c7e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462356"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="66ab1-102">O OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="66ab1-102">The OLE DB Provider for Internet Publishing</span></span>


<span data-ttu-id="66ab1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="66ab1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="66ab1-p101">Os objetos [Record](record-object-ado.md) e [Stream](stream-object-ado.md) do ADO podem ser utilizados com o Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) para acessar e manipular os recursos, como arquivos ou pastas da Web atendidos pelo Microsoft FrontPage. Com o ADO, você pode especificar a origem de um **Record**, **Stream** ou [Recordset](recordset-object-ado.md) que será uma URL. Em seguida, você pode fazer upload, baixar, mover, copiar e excluir os recursos, ou manipular diretamente as propriedades de recursos.</span><span class="sxs-lookup"><span data-stu-id="66ab1-p101">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as Web folders or files served by Microsoft FrontPage. With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL. You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="66ab1-107">Por exemplo, codifique usando **Records** e **Streams** com o Internet Publishing Provider, consulte o [Cenário de publicação na Internet](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="66ab1-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="66ab1-p102">O Internet Publishing Provider é instalado com o Microsoft Windows 2000. As versões anteriores do Internet Publishing Provider também estão disponíveis com o Microsoft Office 2000 e o Microsoft Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="66ab1-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="66ab1-110">Há três maneiras de se conectar o ADO ao Internet Publishing Provider:</span><span class="sxs-lookup"><span data-stu-id="66ab1-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="66ab1-p103">Especifique "URL=" na sequência de conexão. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="66ab1-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="66ab1-113">Especifique Msdaipp.dso para a palavra-chave do *provedor* da cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="66ab1-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="66ab1-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="66ab1-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="66ab1-p105">Especifique Msdaipp.dso para a propriedade [Provider](provider-property-ado.md) do objeto [Connection](connection-object-ado.md). Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="66ab1-p105">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object. For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```


> [!NOTE]
> <P><span data-ttu-id="66ab1-117">Se Msdaipp.dso for explicitamente especificado como o valor do provedor, com a palavra-chave do <EM>provedor de</EM> conexão cadeia de caracteres ou com a propriedade <STRONG>Provider</STRONG> , você não pode usar "URL =" na cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="66ab1-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="66ab1-118">Se o fizer, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="66ab1-118">If you do, an error will occur.</span></span> <span data-ttu-id="66ab1-119">Em vez disso, simplesmente especifique a URL, conforme mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="66ab1-119">Instead, simply specify the URL as shown above.</span></span></P>



<span data-ttu-id="66ab1-120">Para obter informações mais específicas sobre o Internet Publishing Provider, consulte [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) ou a documentação do provedor fornecida com o aplicativo de origem com o qual o OLE DB Provider for Internet Publishing foi instalado: Windows 2000, Office 2000 ou Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="66ab1-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

