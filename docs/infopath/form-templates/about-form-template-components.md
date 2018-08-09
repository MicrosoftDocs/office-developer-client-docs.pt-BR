---
title: Sobre os componentes do modelo de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b51361fe-cf29-f890-9876-5aebe15c73e1
description: Modelos de formulário do Microsoft InfoPath são compostos de vários arquivos e componentes que são combinados para fornecer funcionalidade específica para um determinado usuário final cenário ou necessidade de negócios. Os formulários do InfoPath podem variar em complexidade dependendo do tipo de necessidade que se referem.
ms.openlocfilehash: 4ef90d3fb55ee38018d2c1226bef5fd59e277186
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765587"
---
# <a name="about-form-template-components"></a>Sobre os componentes do modelo de formulário

Modelos de formulário do Microsoft InfoPath são compostos de vários arquivos e componentes que são combinados para fornecer funcionalidade específica para um determinado usuário final cenário ou necessidade de negócios. Os formulários do InfoPath podem variar em complexidade dependendo do tipo de necessidade que se referem.
  
Um modelo de formulário do InfoPath é essencialmente um tipo de aplicativo que cria uma classe específica de documentos XML, define seu layout e o comportamento de edição, impõe sua consistência de dados e fornece as informações de roteamento que indica onde eles devem ser armazenado.
  
É importante entender que os modelos de formulário do InfoPath são compostos de vários arquivos de diversos tipos; Esses arquivos são conhecidos coletivamente como os arquivos de formulário. Geralmente, um modelo de formulário do InfoPath é composto dos seguintes tipos de arquivos.
  
|**Name**|**Extensão**|**Descrição**|
|:-----|:-----|:-----|
|Definição de formulário  <br/> |. xsf  <br/> |Um arquivo gerado pelo InfoPath que contém informações sobre todos os outros arquivos e componentes usados em um formulário. Esse arquivo serve como o manifesto do formulário.  <br/> |
|Esquema XML  <br/> |. xsd  <br/> |Os arquivos de esquema XML que são usados para restringir e validar arquivos de documento XML subjacentes de um formulário.  <br/> |
|Exibir  <br/> |. xsl  <br/> |Os arquivos de lógica de apresentação que são usados para apresentar, exibir e transformar os dados contidos em arquivos de documento XML subjacentes de um formulário.  <br/> |
|Modelo XML  <br/> |. XML  <br/> |O arquivo. XML que contém os dados padrão que são exibidos no modo de exibição quando um novo formulário é criado.  <br/> |
|Apresentação  <br/> |. htm,. gif,. bmp e outras pessoas  <br/> |Os arquivos que são usados em conjunto com os arquivos de modo de exibição para criar uma interface de usuário personalizada.  <br/> |
|Lógica de negócios  <br/> |. dll  <br/> |O código de programação compilado usado para implementar o comportamento de edição específico, validação de dados, manipuladores de eventos, controle de fluxo de dados e outra lógica corporativa personalizada. Lógica de negócios do InfoPath pode ser escrita em Visual Basic e c# .NET linguagens de programação, que são compiladas e incluídas como arquivos binários.  <br/> |
|Binário  <br/> |. dll, .exe  <br/> | Quaisquer componentes personalizados que fornecem lógica de negócios adicionais.  <br/> |
|Modelo de formulário  <br/> |. xsn  <br/> |O formato de arquivo compactado (. cab) que empacota todos os arquivos de formulário em um arquivo.  <br/> |
   

