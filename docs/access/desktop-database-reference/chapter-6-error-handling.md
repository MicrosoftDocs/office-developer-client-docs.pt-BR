---
title: 'Capítulo 6: Tratamento de erros'
TOCTitle: 'Chapter 6: Error handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14d3dc4b291d96a47e0fb67c0e7d837463cd4bf2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296406"
---
# <a name="chapter-6-error-handling"></a><span data-ttu-id="b857d-102">Capítulo 6: Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="b857d-102">Chapter 6: Error handling</span></span>

<span data-ttu-id="b857d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b857d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b857d-p101">O ADO usa vários métodos para notificar um aplicativo sobre os erros ocorridos. Este capítulo aborda os tipos de erros que podem ocorrer quando você usa o ADO e como seu aplicativo é notificado. No final, ele apresenta sugestões sobre como tratar esses erros.</span><span class="sxs-lookup"><span data-stu-id="b857d-p101">ADO uses several different methods to notify an application of errors that occur. This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified. It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="b857d-107">Como o ADO relata erros?</span><span class="sxs-lookup"><span data-stu-id="b857d-107">How does ADO report errors?</span></span>

<span data-ttu-id="b857d-108">O ADO notifica-o sobre erros de diversas maneiras:</span><span class="sxs-lookup"><span data-stu-id="b857d-108">ADO notifies you about errors in several ways:</span></span>

- <span data-ttu-id="b857d-p102">Os erros do ADO geram um erro de tempo de execução. Trate um erro do ADO da mesma maneira que trataria qualquer outro erro de tempo de execução como, por exemplo, usando uma instrução **On Error** do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b857d-p102">ADO errors generate a run-time error. Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

- <span data-ttu-id="b857d-p103">Seu programa pode receber erros do OLE DB. Um erro do OLE DB também gera um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b857d-p103">Your program can receive errors from OLE DB. An OLE DB error generates a run-time error as well.</span></span>

- <span data-ttu-id="b857d-113">Se o erro for específico do provedor de dados, um ou mais objetos **Error** serão incluídos na coleção **Errors** do objeto **Connection** que foi usado para acessar o repositório de dados quando o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b857d-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

- <span data-ttu-id="b857d-p104">Se o processo que gerou um evento também produziu um erro, as informações sobre o erro serão incluídas em um objeto **Error** e passadas como um parâmetro para o evento. Consulte o [Capítulo 7: Tratando eventos do ADO](chapter-7-handling-ado-events.md) para obter mais informações sobre eventos.</span><span class="sxs-lookup"><span data-stu-id="b857d-p104">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event. See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

- <span data-ttu-id="b857d-p105">Os problemas que ocorrem durante o processamento de atualizações em lotes ou outras operações em massa que envolvem um **Recordset** podem ser indicados pela propriedade **Status** do **Recordset**. Por exemplo, violações de restrições de esquema ou permissões insuficientes podem ser especificadas por valores **RecordStatusEnum**.</span><span class="sxs-lookup"><span data-stu-id="b857d-p105">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**. For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

- <span data-ttu-id="b857d-p106">Os problemas ocorridos que envolvem um **Field** específico no registro atual também são indicados pela propriedade **Status** de cada **Field** na coleção **Fields** do **Record** ou **Recordset**. Por exemplo, as atualizações que não puderam ser concluídas ou os tipos de dados incompatíveis podem ser especificados por valores **FieldStatusEnum**.</span><span class="sxs-lookup"><span data-stu-id="b857d-p106">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**. For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="b857d-120">As seções a seguir descrevem cada um desses métodos de notificação em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="b857d-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="b857d-121">Erros do ADO</span><span class="sxs-lookup"><span data-stu-id="b857d-121">ADO errors</span></span>](ado-errors.md)
- [<span data-ttu-id="b857d-122">Referência de erros do ADO</span><span class="sxs-lookup"><span data-stu-id="b857d-122">ADO error reference</span></span>](ado-error-reference.md)
- [<span data-ttu-id="b857d-123">Erros do provedor</span><span class="sxs-lookup"><span data-stu-id="b857d-123">Provider errors</span></span>](provider-errors.md)
- [<span data-ttu-id="b857d-124">Informações de erro relacionado ao campo</span><span class="sxs-lookup"><span data-stu-id="b857d-124">Field-related error information</span></span>](field-related-error-information.md)
- [<span data-ttu-id="b857d-125">Informações de erro relacionado ao conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b857d-125">Recordset-related error information</span></span>](recordset-related-error-information.md)
- [<span data-ttu-id="b857d-126">Antecipação de erros</span><span class="sxs-lookup"><span data-stu-id="b857d-126">Anticipating errors</span></span>](anticipating-errors.md)
- [<span data-ttu-id="b857d-127">Tratamento de erros em outros idiomas (ADO)</span><span class="sxs-lookup"><span data-stu-id="b857d-127">Handling errors in other languages (ADO)</span></span>](handling-errors-in-other-languages.md)
