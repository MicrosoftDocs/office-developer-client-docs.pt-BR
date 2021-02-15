---
title: O OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314053"
---
# <a name="ole-db-provider-for-internet-publishing"></a><span data-ttu-id="406cf-102">OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="406cf-102">OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="406cf-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="406cf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="406cf-104">Os objetos [Record](record-object-ado.md) e [Stream](stream-object-ado.md) do ADO podem ser usados com o Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) para acessar e manipular recursos, como pastas da Web ou arquivos servidos pelo Microsoft FrontPage.</span><span class="sxs-lookup"><span data-stu-id="406cf-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="406cf-105">Com o ADO, você pode especificar a origem de um **Record**, **Stream** ou [Recordset](recordset-object-ado.md) que será uma URL.</span><span class="sxs-lookup"><span data-stu-id="406cf-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="406cf-106">Em seguida, você pode fazer upload, baixar, mover, copiar e excluir os recursos, ou manipular diretamente as propriedades de recursos.</span><span class="sxs-lookup"><span data-stu-id="406cf-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="406cf-107">Por exemplo, codifique usando **Records** e **Streams** com o Internet Publishing Provider, consulte o [Cenário de publicação na Internet](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="406cf-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="406cf-p102">O Internet Publishing Provider é instalado com o Microsoft Windows 2000. As versões anteriores do Internet Publishing Provider também estão disponíveis com o Microsoft Office 2000 e o Microsoft Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="406cf-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="406cf-110">Há três maneiras de se conectar o ADO ao Internet Publishing Provider:</span><span class="sxs-lookup"><span data-stu-id="406cf-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="406cf-p103">Especifique "URL=" na sequência de conexão. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="406cf-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="406cf-113">Especifique Msdaipp.dso para a palavra-chave *Provider* da sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="406cf-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="406cf-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="406cf-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="406cf-115">Especifique Msdaipp.dso para a propriedade [Provider](provider-property-ado.md) do objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="406cf-115">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="406cf-116">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="406cf-116">For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> <span data-ttu-id="406cf-117">Se Msdaipp.dso for explicitamente especificado como o valor do provedor, com a palavra-chave de sequência de conexão *Provider* ou a propriedade **Provider**, você não poderá utilizar "URL=" na sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="406cf-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="406cf-118">Se o fizer, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="406cf-118">If you do, an error will occur.</span></span> <span data-ttu-id="406cf-119">Em vez disso, basta especificar a URL, conforme mostrado anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="406cf-119">Instead, simply specify the URL as shown earlier in this topic.</span></span>

<span data-ttu-id="406cf-120">Para obter informações mais específicas sobre o Internet Publishing Provider, consulte [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) ou a documentação do provedor fornecida com o aplicativo de origem com o qual o OLE DB Provider for Internet Publishing foi instalado: Windows 2000, Office 2000 ou Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="406cf-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

