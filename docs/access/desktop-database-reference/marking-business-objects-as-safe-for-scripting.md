---
title: Marcação de objetos Business como confiáveis para script
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289774"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="24f3e-102">Marcação de objetos Business como confiáveis para script</span><span class="sxs-lookup"><span data-stu-id="24f3e-102">Marking business objects as safe for scripting</span></span>

<span data-ttu-id="24f3e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24f3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24f3e-p101">Para ajudar a assegurar um ambiente seguro de Internet, você precisa marcar todos os objetos de negócios instanciados com o método [CreateObject](dataspace-object-rds.md) do objeto [RDS.DataSpace](createobject-method-rds.md) como "seguro para script". Você precisa se assegurar de que estejam marcados dessa forma na área de Licença no Registro do sistema antes que possam ser utilizados no DCOM.</span><span class="sxs-lookup"><span data-stu-id="24f3e-p101">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting." You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="24f3e-p102">Para marcar manualmente seu objeto de negócios como seguro para script, crie um arquivo de texto com uma extensão .reg que contenha o seguinte texto. Os dois números a seguir permitem o recurso seguro-para-script:</span><span class="sxs-lookup"><span data-stu-id="24f3e-p102">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text. The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="24f3e-108">onde \< *MyActiveXGUID* \> é o número GUID hexadecimal do seu objeto de negócios.</span><span class="sxs-lookup"><span data-stu-id="24f3e-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="24f3e-109">Salve-o e misture-o em seu registro, usando o Editor de Registro ou dando um clique duplo no arquivo .reg no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="24f3e-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="24f3e-110">Os objetos de negócios criados no Microsoft Visual Basic podem ser automaticamente marcados como "seguros para scripts" com o Assistente de Pacote e Implantação.</span><span class="sxs-lookup"><span data-stu-id="24f3e-110">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</span></span> <span data-ttu-id="24f3e-111">Quando o assistente solicitar que especifique as definições de segurança, selecione **Seguro para Inicialização** e **Seguro para Script**.</span><span class="sxs-lookup"><span data-stu-id="24f3e-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="24f3e-p105">Na última etapa, o assistente de configuração do aplicativo cria um arquivo .htm e um arquivo .cab. Em seguida, você pode copiar esses dois arquivos para o computador de destino e dar um clique duplo no arquivo .htm para carregar a página e registrar corretamente o servidor.</span><span class="sxs-lookup"><span data-stu-id="24f3e-p105">On the last step, the Application Setup Wizard creates an .htm and a .cab file. You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="24f3e-114">Como o objeto de negócios será instalado no diretório Occache do Windows System32 por padrão, mova-o para o diretório do Windows System32 e altere a chave de registro \\ \\ \\ **HKEY \_ CLASSES ROOT \_ \\ CLSID \\** \< *MyActiveXGUID* \> \\ **InprocServer32** para corresponder ao caminho correto.</span><span class="sxs-lookup"><span data-stu-id="24f3e-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="24f3e-p106">[!OBSERVAçãO] Os objetos de negócios marcados como seguros para script ou seguros para inicialização podem ser instanciados e inicializados por qualquer pessoa na rede. Qualquer objeto de negócios personalizado não deve ser projetado e implementado casualmente. É obrigatório que tais objetos não representem uma ameaça de segurança que os hackers possam explorar para ganhar acesso à área sensível do servidor hospedeiro e infligir danos.</span><span class="sxs-lookup"><span data-stu-id="24f3e-p106">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network. Any custom business object must not be designed and implemented casually. It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


