---
title: Automatizando o InfoPath de um aplicativo externo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fornece automação de aplicativo do código escrito usando o script e COM usando os métodos do objeto Application e a coleção XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765495"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatizando o InfoPath de um aplicativo externo

Microsoft InfoPath fornece automação de aplicativo do código escrito usando o script e COM usando os métodos do objeto **Application** e a coleção **XDocuments** . 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Visão geral do aplicativo e objetos XDocument

O objeto **Application** contém os seguintes métodos usados para automação: 
  
|**Method**|**Descrição**|
|:-----|:-----|
|**CacheSolution** <br/> |Examina no cache e, se necessário, atualiza a partir do local publicado do modelo de formulário.  <br/> |
|**Quit** <br/> |Encerra o aplicativo do Microsoft Office InfoPath.  <br/> |
|**RegisterSolution** <br/> |Instala o modelo de formulário especificado do Microsoft Office InfoPath.  <br/> |
|**UnregisterSolution** <br/> |Desinstala o modelo de formulário especificado do Microsoft Office InfoPath.  <br/> |
   
A coleção **XDocuments** contém os seguintes métodos que podem ser usados para automação externa: 
  
|**Method**|**Descrição**|
|:-----|:-----|
|Método **Close**  <br/> |Fecha o formulário especificado do Microsoft Office InfoPath.  <br/> |
|Método **New**  <br/> |Cria um novo formulário do Microsoft Office InfoPath.  <br/> |
|Método **NewFromSolution**  <br/> |Cria um novo formulário do Microsoft Office InfoPath com base no modelo de formulário especificado.  <br/> |
|Método **NewFromSolutionWithData**  <br/> |Cria um novo formulário do Microsoft Office InfoPath usando o modelo de formulário e de dados XML especificado.  <br/> |
|Método **Open**  <br/> |Abre o formulário especificado do Microsoft Office InfoPath.  <br/> |
   
Para usar o objeto **Application** de um aplicativo externo, use a função **CreateObject** com o ProgID do aplicativo InfoPath ("InfoPath.Application") para criar uma variável de objeto que representa o aplicativo do InfoPath. Em seguida, você pode usar a propriedade **XDocuments** para acessar a coleção **XDocuments** e usar seus métodos para abrir ou criar um formulário do InfoPath. O exemplo a seguir demonstra a criação de uma referência ao objeto de **aplicativo** usando o Microsoft Visual Basic 6.0 ou o Visual Basic for Applications (VBA) linguagem de programação: 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Como a função **CreateObject** cria uma variável de objeto usando a associação tardia, conclusão da instrução automática não estará disponível no Editor do Visual Basic. Consulte os links nas tabelas anteriores para obter informações sobre a sintaxe correta de chamada. 
  

