---
title: InfoPath, codificação RPC e serviços Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Serviços Web podem expor um dos dois estilos de associação para seus métodos Web no contrato da Linguagem de Descrição de Serviço Web (WSDL) que os descreve: RPC ou documento.'
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303525"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="ed1f3-103">InfoPath, codificação RPC e serviços Web</span><span class="sxs-lookup"><span data-stu-id="ed1f3-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="ed1f3-104">Serviços Web podem expor um dos dois estilos de associação para seus métodos Web no contrato da Linguagem de Descrição de Serviço Web (WSDL) que os descreve: RPC ou documento.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-104">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC.</span></span> <span data-ttu-id="ed1f3-105">Além disso, cada um desses dois estilos de associação pode ser especificado como literal ou codificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-105">Additionally, each of these two styles of binding can be specified as either literal or encoded.</span></span> <span data-ttu-id="ed1f3-106">Implementações mais comuns para cada tipo são: documento/literal e RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-106">The most common implementations for each type are: document/literal and RPC/encoded.</span></span> <span data-ttu-id="ed1f3-107">No entanto, o Microsoft InfoPath apenas dá suporte à conexão de serviços Web com o estilo de documento/literal.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-107">However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="ed1f3-108">A maioria das ferramentas de desenvolvimento do serviço Web fornecem uma opção para especificar o tipo de serviço Web que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-108">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create.</span></span> <span data-ttu-id="ed1f3-109">Se estiver desenvolvendo um serviço Web que se conectará ao InfoPath, você deverá especificar o estilo e a codificação do seu serviço Web como documento/literal.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-109">If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="ed1f3-110">No entanto, se você não controla o serviço Web que deseja usar e precisa se conectar a um serviço Web, usando o estilo RPC/codificado, use o serviço proxy do .NET para se conectar a um serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="ed1f3-111">Usar um serviço proxy do .NET para se conectar a um serviço Web</span><span class="sxs-lookup"><span data-stu-id="ed1f3-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="ed1f3-112">Caso não controle o serviço Web RPC/codificado que deseja usar, você poderá criar um proxy de documento/literal de serviço Web do Microsoft .NET que forneça funções de conteúdo adicional para cada um dos métodos Web que você deseja invocar do serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-112">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service.</span></span> <span data-ttu-id="ed1f3-113">Você pode trabalhar com o serviço Web documento/literal do proxy no InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-113">You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="ed1f3-114">O código do .NET Framework pode trabalhar com qualquer tipo de serviço Web (RPC/codificado e documento/literal), e todos os serviços Web do .NET usam o estilo e a codificação documento/literal.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-114">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding.</span></span> <span data-ttu-id="ed1f3-115">Como o .NET Framework pode se comunicar com qualquer tipo de serviço Web, você pode criar um serviço Web com métodos para fazer chamadas ao serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-115">Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service.</span></span> <span data-ttu-id="ed1f3-116">O serviço Web .NET atuará como um tradutor que permite que o InfoPath faça chamadas do estilo documento/literal para o serviço Web do .NET, que por sua vez pode fazer chamadas com o estilo RPC/codificado para o serviço Web original.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-116">The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="ed1f3-117">Os pré-requisitos para criar um serviço Web proxy do Microsoft .NET são um computador Microsoft Windows ou Microsoft Windows Server com o IIS (Serviços de Informações de Internet) instalado, onde será possível implantar o proxy de serviço Web do ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-117">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service.</span></span> <span data-ttu-id="ed1f3-118">Ao criar uma solução do InfoPath, você apontará para o serviço Web proxy em vez do serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-118">When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service.</span></span> <span data-ttu-id="ed1f3-119">O serviço Web proxy fará chamadas ao serviço RPC/codifificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-119">The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="ed1f3-120">Criar um serviço Web proxy usando o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ed1f3-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="ed1f3-121">Crie um novo projeto de **aplicativo de serviços Web do ASP.NET**.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-121">Create a new **ASP.NET Web Service Application** project.</span></span> 
    
2. <span data-ttu-id="ed1f3-122">No **Explorador de Soluções**, clique com o botão direito do mouse na pasta **Referências** de seu novo projeto e clique em **Adicionar Referência da Web**.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="ed1f3-123">Na caixa de diálogo **Adicionar Referência da Web**, digite a URL do serviço Web RPC/codificado que você deseja usar e clique em **Ir**.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="ed1f3-124">Clique em **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="ed1f3-125">Abra o arquivo. asmx do seu serviço Web e adicione um método de serviço Web para chamar cada método de serviço Web que usa o serviço Web RPC/codificado referenciado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="ed1f3-126">Para exibir uma lista dos métodos no servidor Web RPC/codificado de referência, exiba a janela **Modo de Exibição de Classe**.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-126">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window.</span></span> <span data-ttu-id="ed1f3-127">Para cada método de serviço Web, você verá três métodos.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-127">For each Web Service method, you will see three methods.</span></span> <span data-ttu-id="ed1f3-128">Por exemplo, se o método de serviço Web for acionado `doSearch`, você verá três métodos chamados `doSearch`, `BegindoSearch` e `EnddoSearch`.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-128">For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`.</span></span> <span data-ttu-id="ed1f3-129">Você só precisa criar um método de serviço Web de conteúdo adicional para o método `doSearch`.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-129">You only have to create a wrapper Web Service method for the  `doSearch` method.</span></span> <span data-ttu-id="ed1f3-130">Certifique-se de combinar o método exato de assinatura com o tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-130">Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="ed1f3-131">Em cada método de conteúdo adicional, você precisa escrever o código para fazer uma chamada ao serviço Web RPC/codificado referenciado, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="ed1f3-132">Se o serviço Web RPC/codificado requerer autenticação, codifique as credenciais necessárias para conectar o serviço Web RPC/codificado ao código fonte do serviço Web proxy do .NET, ou você pode usar um código como o do exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="ed1f3-133">Para saber mais, procure o artigo da Base de Conhecimento Microsoft "Como: passar as credenciais atuais para um serviço Web ASP.NET" em https://support.microsoft.com/.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on https://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="ed1f3-134">Criar um serviço Web proxy sem usar o Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="ed1f3-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="ed1f3-135">Como alternativa, você pode criar um serviço Web proxy usando as ferramentas que são fornecidas com o .NET Framework SDK, que pode ser baixado no MSDN.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="ed1f3-136">Use a Ferramenta de Linguagem de Descrição de Serviços Web (Wsdl.exe) para criar o arquivo de código do serviço Web proxy.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-136">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service.</span></span> <span data-ttu-id="ed1f3-137">Esse arquivo de código pode ser compilado usando a linha de comando do compilador C# (csc.exe) ou o compilador de linha de comando .NET do Visual Basic (vbc.exe), que também está incluído no SDK do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-137">This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK.</span></span> <span data-ttu-id="ed1f3-138">Depois que a ferramenta WSDL tiver gerado o arquivo de código, renomeie a extensão de nome de arquivo para. asmx e abra o arquivo em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-138">After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor.</span></span> <span data-ttu-id="ed1f3-139">Na primeira linha do documento, adicione a diretiva de página a seguir:</span><span class="sxs-lookup"><span data-stu-id="ed1f3-139">On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="ed1f3-140">Vá até o final do arquivo de código para criar uma chamada para cada método de serviço Web no serviço Web RPC/codificado.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-140">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service.</span></span> <span data-ttu-id="ed1f3-141">O exemplo a seguir mostra o código de um serviço Web que se conecta ao serviço Web do Google, que usa o estilo RPC/codificado de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-141">The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development.</span></span> <span data-ttu-id="ed1f3-142">Há um espaço reservado para onde o código gerado wsdl.exe deve ir.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-142">There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
 
using System; 
using System.Web.Services; 
 
// The auto-generated code from the wsdl.exe tool goes here. 
 
[WebService] 
public class GoogleSearchServiceWrapper : System.Web.Services.WebService  
{ 
    [WebMethod] 
    public System.Byte[] doGetCachedPage(System.String key, System.String url) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doGetCachedPage(key, url); 
    } 
 
    [WebMethod] 
    public System.String doSpellingSuggestion(System.String key, System.String phrase) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doSpellingSuggestion(key, phrase); 
    } 
 
    [WebMethod] 
    public GoogleSearchResult doGoogleSearch(System.String key, 
      System.String q, 
      System.Int32 start, 
      System.Int32 maxResults, 
      System.Boolean filter, 
      System.String restrict, 
      System.Boolean safeSearch, 
      System.String lr, 
      System.String ie, 
      System.String oe) 
    {
        GoogleSearchService srch = new GoogleSearchService();
           return srch.doGoogleSearch(key, q, start, maxResults, 
               filter, restrict, safeSearch, lr, ie, oe); 
    } 
}
```


