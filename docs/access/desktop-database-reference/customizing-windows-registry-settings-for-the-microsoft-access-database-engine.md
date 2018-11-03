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
ms.openlocfilehash: 99e2b31cf686895a56e9d70b177314355c1aff3c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945142"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="46cba-102">Personalização das configurações do Registro do Windows para o mecanismo de banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="46cba-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="46cba-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="46cba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46cba-104">Se seu aplicativo não pode funcionar corretamente com a funcionalidade padrão do mecanismo de banco de dados do Microsoft Access, você pode precisar alterar as configurações no registro do Microsoft Windows para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="46cba-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="46cba-105">O Registro do Windows também pode ser usado para ajustar a operação do driver ISAM e ODBC instalável.</span><span class="sxs-lookup"><span data-stu-id="46cba-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="46cba-106">Você pode personalizar as configurações do Registro do Windows de quatro maneiras diferentes:</span><span class="sxs-lookup"><span data-stu-id="46cba-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- <span data-ttu-id="46cba-107">[Usando Regedit.exe para substituir as configurações padrão](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="46cba-107">[Using Regedit.exe to overwrite the default settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>
- <span data-ttu-id="46cba-108">[Criando uma parte da árvore de registro do seu aplicativo para gerenciar as configurações](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="46cba-108">[Creating a portion in your application's registry tree to manage the settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>
- <span data-ttu-id="46cba-109">[Usando o método SetOption a partir do DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="46cba-109">[Using the SetOption method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>
- <span data-ttu-id="46cba-110">[Uso das propriedades de Conexão do Microsoft OLE DB Provider para acesso](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="46cba-110">[Using the Connection properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

