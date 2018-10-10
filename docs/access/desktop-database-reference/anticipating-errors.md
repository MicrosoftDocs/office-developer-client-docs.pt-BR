---
title: Prevendo erros
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f062eb86b45778cc7f25fb2d0d0588b82bdd78b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464576"
---
# <a name="anticipating-errors"></a><span data-ttu-id="96b59-102">Prevendo erros</span><span class="sxs-lookup"><span data-stu-id="96b59-102">Anticipating Errors</span></span>


<span data-ttu-id="96b59-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="96b59-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="96b59-p101">A prevenção de erros é tão importante quanto o tratamento de erros. Esta seção final contém uma pequena lista de precauções que podem ser tomadas pelo aplicativo para ajudar a diminuir a probabilidade de ocorrência de erros.</span><span class="sxs-lookup"><span data-stu-id="96b59-p101">Error prevention is at least as important as error handling. This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="96b59-p102">Confira o estado dos objetos verificando o valor da propriedade **State** antes de tentar executar uma operação usando esses objetos. Por exemplo, se o aplicativo usar uma **Conexão** global, verifique a respectiva propriedade **State** para ver se ela já está aberta, antes de chamar o método **Open**.</span><span class="sxs-lookup"><span data-stu-id="96b59-p102">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects. For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

  - <span data-ttu-id="96b59-p103">Qualquer programa que aceite dados de um usuário deve incluir código para validar esses dados antes de enviá-los para o repositório. Você não pode contar com o repositório de dados, o provedor, o ADO ou mesmo a sua linguagem de programação para notificá-lo de problemas. É necessário verificar cada byte inserido pelos seus usuários, para ter certeza de que os dados são do tipo correto para o campo e que os campos obrigatórios não estão vazios.</span><span class="sxs-lookup"><span data-stu-id="96b59-p103">Any program that accepts data from a user must include code to validate that data before sending it to the data store. You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems. You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="96b59-p104">Verifique os dados antes de tentar gravá-los no repositório. A maneira mais fácil de fazer isso é manipular o evento **WillMove** ou o evento **WillUpdateRecordset**. Para obter uma abordagem mais completa da manipulação de eventos do ADO, consulte [Capítulo 7: Manipulando eventos do ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="96b59-p104">Check the data before you try to write any data to the data store. The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="96b59-p105">Verifique se os objetos **Recordset** não ultrapassam os limites do **Recordset** antes de tentar mover o ponteiro do registro. Se você tentar **MoveNext** quando **EOF** for True ou tentar **MovePrev** quando **BOF** for True, ocorrerá um erro. Se você executar qualquer um dos métodos **Move** quando **EOF** e **BOF** forem True, será gerado um erro.</span><span class="sxs-lookup"><span data-stu-id="96b59-p105">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer. If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur. If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="96b59-117">Também ocorrerão erros se você tentar executar operações como **Seek** e **Find** em um **Recordset** vazio.</span><span class="sxs-lookup"><span data-stu-id="96b59-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>

