---
title: Personalizando configurações de registro do Windows para o mecanismo de banco de dados do Microsoft Access
TOCTitle: Customizing Windows Registry Settings for the Microsoft Access Database Engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4a90981c936c933d2eadb191bbf0d2639cd8e641
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464565"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="69412-102">Personalizando as configurações do Registro do Windows para o mecanismo de banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="69412-102">Customizing Windows Registry Settings for the Microsoft Access Database Engine</span></span>


<span data-ttu-id="69412-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="69412-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="69412-p101">Se o seu aplicativo não funcionar corretamente com a funcionalidade padrão do mecanismo de banco de dados do Microsoft Access, talvez você tenha que alterar as configurações no Registro do Microsoft® Windows® de acordo com suas necessidades. O Registro do Windows também pode ser usado para ajustar a operação do driver ISAM e ODBC instalável.</span><span class="sxs-lookup"><span data-stu-id="69412-p101">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft® Windows® Registry to suit your needs. The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="69412-106">Você pode personalizar as configurações do Registro do Windows de quatro maneiras diferentes:</span><span class="sxs-lookup"><span data-stu-id="69412-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

<span data-ttu-id="69412-107">[Usando Regedit.exe para substituir as configurações padrão](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="69412-107">[Using Regedit.exe to Overwrite the Default Settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>

<span data-ttu-id="69412-108">[Criando uma parte da árvore de registros do aplicativo para gerenciar as configurações](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="69412-108">[Creating a Portion in Your Application's Registry Tree to Manage the Settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>

<span data-ttu-id="69412-109">[Usando o Método SetOption do DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="69412-109">[Using the SetOption Method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>

<span data-ttu-id="69412-110">[Usando as propriedades de conexão do Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="69412-110">[Using the Connection Properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

