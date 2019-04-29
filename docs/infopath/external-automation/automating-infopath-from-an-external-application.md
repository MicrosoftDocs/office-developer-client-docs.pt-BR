---
title: Automatizar o InfoPath desde aplicativos externos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: O Microsoft InfoPath fornece automação de aplicativo a partir de código escrito usando COM e script usando métodos do objeto Application e a coleção XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412664"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatizar o InfoPath desde aplicativos externos

O Microsoft InfoPath fornece automação de aplicativo a partir de código escrito usando COM e script usando métodos do objeto **Application** e a coleção **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Visão geral dos objetos Application e XDocument

O objeto **Application** contém os seguintes métodos usados para automação: 
  
|**Method**|**Descrição**|
|:-----|:-----|
|**CacheSolution** <br/> |Examina o no cache e, se necessário, o atualiza a partir do local publicado do modelo de formulário.  <br/> |
|**Quit** <br/> |Encerra o aplicativo Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Instala o modelo de formulário do Microsoft Office InfoPath especificado.  <br/> |
|**UnregisterSolution** <br/> |Desinstala o modelo de formulário do Microsoft Office InfoPath especificado.  <br/> |
   
A **** coleção XDocuments contém os seguintes métodos que podem ser usados para automação externa: 
  
|**Method**|**Descrição**|
|:-----|:-----|
|Método **Close**  <br/> |Fecha o formulário do Microsoft Office InfoPath especificado.  <br/> |
|**Novo** método  <br/> |Cria um novo formulário do Microsoft Office InfoPath.  <br/> |
|Método **NewFromSolution**  <br/> |Cria um novo formulário do Microsoft Office InfoPath com base no modelo de formulário especificado.  <br/> |
|Método **NewFromSolutionWithData**  <br/> |Cria um novo formulário do Microsoft Office InfoPath usando os dados XML e o modelo de formulário especificados.  <br/> |
|Método **Open**  <br/> |Abre o formulário do Microsoft Office InfoPath especificado.  <br/> |
   
Para usar o objeto **Application** de um aplicativo externo, use a função **CreateObject** com o ProgID do aplicativo InfoPath ("InfoPath. Application") para criar uma variável de objeto que represente o aplicativo InfoPath. Você pode usar a propriedade **XDocuments** para acessar a coleção **XDocuments** e usar seus métodos para abrir ou criar um formulário do InfoPath. O exemplo a seguir demonstra a criação de uma referência ao objeto **Application** usando a linguagem de programação Microsoft visual Basic 6,0 ou Visual Basic for Applications (VBA): 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Como a função **CreateObject** cria uma variável de objeto usando associação tardia, a conclusão automática da instrução não estará disponível no editor do Visual Basic. Consulte os links nas tabelas anteriores para obter informações sobre a sintaxe de chamada correta. 
  

