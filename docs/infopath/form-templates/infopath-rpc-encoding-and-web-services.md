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
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath, codificação RPC e serviços Web

Serviços Web podem expor um dos dois estilos de associação para seus métodos Web no contrato da Linguagem de Descrição de Serviço Web (WSDL) que os descreve: RPC ou documento. Além disso, cada um desses dois estilos de associação pode ser especificado como literal ou codificado. Implementações mais comuns para cada tipo são: documento/literal e RPC/codificado. No entanto, o Microsoft InfoPath apenas dá suporte à conexão de serviços Web com o estilo de documento/literal.
  
A maioria das ferramentas de desenvolvimento do serviço Web fornecem uma opção para especificar o tipo de serviço Web que você deseja criar. Se estiver desenvolvendo um serviço Web que se conectará ao InfoPath, você deverá especificar o estilo e a codificação do seu serviço Web como documento/literal.
  
No entanto, se você não controla o serviço Web que deseja usar e precisa se conectar a um serviço Web, usando o estilo RPC/codificado, use o serviço proxy do .NET para se conectar a um serviço Web RPC/codificado.
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>Usar um serviço proxy do .NET para se conectar a um serviço Web

Caso não controle o serviço Web RPC/codificado que deseja usar, você poderá criar um proxy de documento/literal de serviço Web do Microsoft .NET que forneça funções de conteúdo adicional para cada um dos métodos Web que você deseja invocar do serviço Web RPC/codificado. Você pode trabalhar com o serviço Web documento/literal do proxy no InfoPath.
  
O código do .NET Framework pode trabalhar com qualquer tipo de serviço Web (RPC/codificado e documento/literal), e todos os serviços Web do .NET usam o estilo e a codificação documento/literal. Como o .NET Framework pode se comunicar com qualquer tipo de serviço Web, você pode criar um serviço Web com métodos para fazer chamadas ao serviço Web RPC/codificado. O serviço Web .NET atuará como um tradutor que permite que o InfoPath faça chamadas do estilo documento/literal para o serviço Web do .NET, que por sua vez pode fazer chamadas com o estilo RPC/codificado para o serviço Web original.
  
Os pré-requisitos para criar um serviço Web proxy do Microsoft .NET são um computador Microsoft Windows ou Microsoft Windows Server com o IIS (Serviços de Informações de Internet) instalado, onde será possível implantar o proxy de serviço Web do ASP.NET. Ao criar uma solução do InfoPath, você apontará para o serviço Web proxy em vez do serviço Web RPC/codificado. O serviço Web proxy fará chamadas ao serviço RPC/codifificado.
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Criar um serviço Web proxy usando o Visual Studio

1. Crie um novo projeto de **aplicativo de serviços Web do ASP.NET**. 
    
2. No **Explorador de Soluções**, clique com o botão direito do mouse na pasta **Referências** de seu novo projeto e clique em **Adicionar Referência da Web**. 
    
3. Na caixa de diálogo **Adicionar Referência da Web**, digite a URL do serviço Web RPC/codificado que você deseja usar e clique em **Ir**.
    
4. Clique em **Adicionar Referência**. 
    
5. Abra o arquivo. asmx do seu serviço Web e adicione um método de serviço Web para chamar cada método de serviço Web que usa o serviço Web RPC/codificado referenciado.
    
6. Para exibir uma lista dos métodos no servidor Web RPC/codificado de referência, exiba a janela **Modo de Exibição de Classe**. Para cada método de serviço Web, você verá três métodos. Por exemplo, se o método de serviço Web for acionado `doSearch`, você verá três métodos chamados `doSearch`, `BegindoSearch` e `EnddoSearch`. Você só precisa criar um método de serviço Web de conteúdo adicional para o método `doSearch`. Certifique-se de combinar o método exato de assinatura com o tipo de retorno. 
    
7. Em cada método de conteúdo adicional, você precisa escrever o código para fazer uma chamada ao serviço Web RPC/codificado referenciado, conforme mostrado no exemplo a seguir. 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. Se o serviço Web RPC/codificado requerer autenticação, codifique as credenciais necessárias para conectar o serviço Web RPC/codificado ao código fonte do serviço Web proxy do .NET, ou você pode usar um código como o do exemplo a seguir. 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

Para saber mais, procure o artigo da Base de Conhecimento Microsoft "Como: passar as credenciais atuais para um serviço Web ASP.NET" em https://support.microsoft.com/.
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Criar um serviço Web proxy sem usar o Visual Studio .NET

Como alternativa, você pode criar um serviço Web proxy usando as ferramentas que são fornecidas com o .NET Framework SDK, que pode ser baixado no MSDN.
  
Use a Ferramenta de Linguagem de Descrição de Serviços Web (Wsdl.exe) para criar o arquivo de código do serviço Web proxy. Esse arquivo de código pode ser compilado usando a linha de comando do compilador C# (csc.exe) ou o compilador de linha de comando .NET do Visual Basic (vbc.exe), que também está incluído no SDK do .NET Framework. Depois que a ferramenta WSDL tiver gerado o arquivo de código, renomeie a extensão de nome de arquivo para. asmx e abra o arquivo em um editor de texto. Na primeira linha do documento, adicione a diretiva de página a seguir:
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

Vá até o final do arquivo de código para criar uma chamada para cada método de serviço Web no serviço Web RPC/codificado. O exemplo a seguir mostra o código de um serviço Web que se conecta ao serviço Web do Google, que usa o estilo RPC/codificado de desenvolvimento. Há um espaço reservado para onde o código gerado wsdl.exe deve ir.
  
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


