---
title: Implementar a interface IClassFactory para servidores de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310028"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="c1cac-103">Implementar a interface IClassFactory para servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="c1cac-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="c1cac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1cac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1cac-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) é a interface OLE que os aplicativos cliente usam para criar novos objetos de formulário da classe de mensagens do seu servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="c1cac-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="c1cac-106">A tabela a seguir lista os métodos **IClassFactory** que são necessários.</span><span class="sxs-lookup"><span data-stu-id="c1cac-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="c1cac-107">**Método**</span><span class="sxs-lookup"><span data-stu-id="c1cac-107">**Method**</span></span>|<span data-ttu-id="c1cac-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c1cac-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1cac-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="c1cac-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="c1cac-110">Cria um novo objeto Form.</span><span class="sxs-lookup"><span data-stu-id="c1cac-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="c1cac-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="c1cac-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="c1cac-112">Bloqueia o servidor de formulário na memória para que a sobrecarga de inicialização possa ser evitada quando vários objetos de formulário são criados.</span><span class="sxs-lookup"><span data-stu-id="c1cac-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="c1cac-113">Para todas as informações necessárias para implementar esses métodos, consulte a seção de serviços de objeto COM e ActiveX no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c1cac-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1cac-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1cac-114">See also</span></span>



[<span data-ttu-id="c1cac-115">Gravando código de servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="c1cac-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

