---
title: O que é um bloqueio? (Referência de banco de dados da área de trabalho do access)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f852901be41060568bdbad539906e9166d080fad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463816"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="34a5b-103">O que é um bloqueio?</span><span class="sxs-lookup"><span data-stu-id="34a5b-103">What is a Lock?</span></span>


<span data-ttu-id="34a5b-104">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a5b-104">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34a5b-p102">Bloqueio é o processo pelo qual um DBMS restringe o acesso a uma linha em um ambiente com vários usuários. Quando uma linha ou coluna é bloqueada exclusivamente, outros usuários não têm permissão para acessar os dados bloqueados até que o bloqueio seja liberado. Isso garante que dois usuários não possam atualizar a mesma coluna simultaneamente em uma linha.</span><span class="sxs-lookup"><span data-stu-id="34a5b-p102">Locking is the process by which a DBMS restricts access to a row in a multi-user environment. When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released. This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="34a5b-p103">Os bloqueios podem ser muito onerosos a partir de uma perspectiva do recurso e deveria ser usada apenas quando necessário para preservar a integridade dos dados. Em um banco de dados no qual centenas ou milhares de usuários poderiam estar tentando acessar um registro a cada segundo  como um banco de dados conectado à Internet  o bloqueio desnecessário poderia resultar rapidamente em um desempenho mais lento no seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34a5b-p103">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity. In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="34a5b-110">Você pode controlar como a fonte de dados e a biblioteca de cursor ADO gerenciam a concorrência, escolhendo a opção de bloqueio adequada.</span><span class="sxs-lookup"><span data-stu-id="34a5b-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="34a5b-p104">Defina a propriedade **LockType** antes de abrir um **Recordset** para especificar qual tipo de bloqueio o provedor deveria usar ao abri-lo. Leia a propriedades para retornar o tipo de bloqueio em uso em um objeto **Recordset** aberto.</span><span class="sxs-lookup"><span data-stu-id="34a5b-p104">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="34a5b-p105">Os provedores não podem oferecer suporte a todos os tipos de bloqueio. Se um provedor não puder oferecer suporte à configuração **LockType** solicitada, ele substituirá outro tipo de bloqueio. Para determinar a funcionalidade de bloqueio real disponível em um objeto **Recordset**, use o método [Supports](supports-method-ado.md) com **adUpdate** e **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="34a5b-p105">Providers might not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="34a5b-p106">Não há suporte para a configuração **adLockPessimistic** se a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**. Se um valor sem suporte for definido, nenhum erro ocorrerá; o **LockType** suportado mais próximo será usado.</span><span class="sxs-lookup"><span data-stu-id="34a5b-p106">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="34a5b-118">A propriedade **LockType** é de leitura/gravação quando o **Recordset** está fechado e somente leitura quando está aberto.</span><span class="sxs-lookup"><span data-stu-id="34a5b-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

