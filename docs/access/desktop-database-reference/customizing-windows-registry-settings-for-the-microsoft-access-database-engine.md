---
title: Personalização das configurações do Registro do Windows para o mecanismo de banco de dados do Microsoft Access
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b961869f3add04cf4af827f96721aad6dba611b6
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025599"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="94dff-102">Personalização das configurações do Registro do Windows para o mecanismo de banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="94dff-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="94dff-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="94dff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94dff-104">Se seu aplicativo não pode funcionar corretamente com a funcionalidade padrão do mecanismo de banco de dados do Microsoft Access, você pode precisar alterar as configurações no registro do Microsoft Windows para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="94dff-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="94dff-105">O Registro do Windows também pode ser usado para ajustar a operação do driver ISAM e ODBC instalável.</span><span class="sxs-lookup"><span data-stu-id="94dff-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="94dff-106">Você pode personalizar as configurações do Registro do Windows de quatro maneiras diferentes:</span><span class="sxs-lookup"><span data-stu-id="94dff-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- [<span data-ttu-id="94dff-107">Usando Regedit.exe para substituir as configurações padrão</span><span class="sxs-lookup"><span data-stu-id="94dff-107">Using Regedit.exe to overwrite the default settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [<span data-ttu-id="94dff-108">Criando uma parte da árvore de registro do seu aplicativo para gerenciar as configurações</span><span class="sxs-lookup"><span data-stu-id="94dff-108">Creating a portion in your application's registry tree to manage the settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [<span data-ttu-id="94dff-109">Usando o método SetOption a partir do DAO</span><span class="sxs-lookup"><span data-stu-id="94dff-109">Using the SetOption method from DAO</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [<span data-ttu-id="94dff-110">Uso das propriedades de Conexão do Microsoft OLE DB Provider para acesso</span><span class="sxs-lookup"><span data-stu-id="94dff-110">Using the Connection properties in the Microsoft OLE DB Provider for Access</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

