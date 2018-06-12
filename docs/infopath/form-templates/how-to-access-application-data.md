---
title: Dados de aplicativo do Access
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- nomes de aplicativo [infopath 2007], acessando o nome do aplicativo [InfoPath 2007], InfoPath 2007, acessando dados do aplicativo, acessando a versão do aplicativo [InfoPath 2007], [InfoPath 2007] de versões de aplicativo, IDs de idioma [InfoPath 2007], LCID [InfoPath ID de dados do aplicativo [InfoPath 2007], acessando o idioma de 2007], [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: O InfoPath modelo de objeto de código gerenciado fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário. Esses dados são acessados através do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciado, usando a classe de aplicativo.
ms.openlocfilehash: 3c3f6be4e90e292eb572da836bca0a8dcf1883cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765591"
---
# <a name="access-application-data"></a><span data-ttu-id="99f78-105">Dados de aplicativo do Access</span><span class="sxs-lookup"><span data-stu-id="99f78-105">Access Application Data</span></span>

<span data-ttu-id="99f78-106">O InfoPath modelo de objeto de código gerenciado fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário.</span><span class="sxs-lookup"><span data-stu-id="99f78-106">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="99f78-107">Esses dados são acessados através do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciado, usando a classe de [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="99f78-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="99f78-108">Em um projeto do InfoPath código gerenciado formulário modelo criado usando o Visual Studio 2012, você pode usar a **Este** (c#) ou palavra-chave **Me** (Visual Basic) para acessar uma instância da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que representa o aplicativo atual do InfoPath, que podem ser usados para acessar as propriedades e métodos da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="99f78-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="99f78-109">Example</span><span class="sxs-lookup"><span data-stu-id="99f78-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="99f78-110">Exibir o nome do aplicativo, versão e ID de idioma</span><span class="sxs-lookup"><span data-stu-id="99f78-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="99f78-111">No exemplo a seguir, as propriedades de [nome](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) e a [versão](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) são usadas para retornar o número de nome e a versão da instância em execução do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="99f78-111">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="99f78-112">A propriedade [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) , em seguida, é usada para retornar um objeto **LanguageSettings** , que por sua vez, é usado para retornar o LCID (um número de quatro dígitos) para o idioma que está sendo usado atualmente para o idioma de interface de usuário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="99f78-112">The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language.</span></span> <span data-ttu-id="99f78-113">Finalmente, todas estas informações é exibido em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="99f78-113">Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="99f78-114">Para a propriedade **LanguageSettings** funcionar, você deve estabelecer uma referência à biblioteca de objeto do Microsoft Office 14.0 da guia **COM** da caixa de diálogo **Adicionar referência** no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="99f78-114">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> <span data-ttu-id="99f78-115">Isso irá estabelecer uma referência para o namespace da **Microsoft.Office.Core** , que contém a classe **LanguageSettings** .</span><span class="sxs-lookup"><span data-stu-id="99f78-115">This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class.</span></span> <span data-ttu-id="99f78-116">Além disso, o formulário deve estar executando como confiança total.</span><span class="sxs-lookup"><span data-stu-id="99f78-116">Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="99f78-117">Este exemplo requer um **usando** ou a diretiva de **importações** para o namespace da **Microsoft.Office.Core** na seção Declaração do módulo do formulário de código.</span><span class="sxs-lookup"><span data-stu-id="99f78-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
```cs
string appName = this.Application.Name;
string appVersion = this.Application.Version;
LanguageSettings langSettings = 
   (LanguageSettings)this.Application.LanguageSettings;
int langID = 
   langSettings.get_LanguageID(MsoAppLanaguageID.msoLanguageIDUI);
MessageBox.Show(
   "Name: " + appName + System.Environment.NewLine +
   "Version: " + appVersion + System.Environment.NewLine +
   "Language ID: " + langID);
```

```vb
Dim appName As String appName = Me.Application.Name
Dim appVersion As String = Me.Application.Version
Dim langSettings As LanguageSettings = _
   DirectCast(Me.Application.LanguageSettings, LanguageSettings)
Dim langID As Integer = _
   langSettings.LanguageID(MsoAppLanaguageID.msoLanguageIDUI)
MessageBox.Show( _
   "Name: " + appName + System.Environment.NewLine + _
   "Version: " + appVersion + System.Environment.NewLine + _
   "Language ID: " + langID)
```


