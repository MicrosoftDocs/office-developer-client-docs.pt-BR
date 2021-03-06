---
title: Sobre componentes de modelo de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b51361fe-cf29-f890-9876-5aebe15c73e1
description: Os modelos de formulário do Microsoft InfoPath são compostos de vários arquivos e componentes que são combinados para fornecer funcionalidade específica para um cenário específico do usuário final ou necessidades comerciais. Os formulários do InfoPath podem variar em complexidade, dependendo do tipo de necessidade que eles abordam.
ms.openlocfilehash: 3c5adc7ec1e24af481dff7f4a8d009b2dcb6ba8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419055"
---
# <a name="about-form-template-components"></a>Sobre componentes de modelo de formulário

Os modelos de formulário do Microsoft InfoPath são compostos de vários arquivos e componentes que são combinados para fornecer funcionalidade específica para um cenário específico do usuário final ou necessidades comerciais. Os formulários do InfoPath podem variar em complexidade, dependendo do tipo de necessidade que eles abordam.
  
Um modelo de formulário do InfoPath é essencialmente um tipo de aplicativo que cria uma classe especificada de documentos XML, define seu comportamento de layout e edição, impõe a consistência dos dados e fornece as informações de roteamento que indicam onde eles devem ser armazenados.
  
É importante entender que os modelos de formulário do InfoPath são compostos de vários arquivos diferentes de vários tipos diferentes; esses arquivos são coletivamente conhecidos como arquivos de formulário. Geralmente, um modelo de formulário do InfoPath é composto pelos seguintes tipos de arquivos.
  
|**Nome**|**Extensão**|**Descrição**|
|:-----|:-----|:-----|
|Definição de formulário  <br/> |.xsf  <br/> |Um arquivo gerado pelo InfoPath que contém informações sobre todos os outros arquivos e componentes usados em um formulário. Esse arquivo serve como manifesto para o formulário.  <br/> |
|Esquema XML  <br/> |.xsd  <br/> |Os arquivos de esquema XML usados para restringir e validar os arquivos de documento XML subjacentes de um formulário.  <br/> |
|Exibir  <br/> |.xsl  <br/> |Os arquivos de lógica de apresentação usados para apresentar, exibir e transformar os dados contidos nos arquivos de documento XML subjacentes de um formulário.  <br/> |
|Modelo XML  <br/> |.xml  <br/> |O arquivo .xml que contém os dados padrão exibidos em um modo de exibição quando um novo formulário é criado.  <br/> |
|Presentation  <br/> |.htm, .gif, .bmp e outros  <br/> |Os arquivos usados em conjunto com os arquivos de exibição para criar uma interface do usuário personalizada.  <br/> |
|Lógica comercial  <br/> |.dll  <br/> |O código de programação compilado usado para implementar comportamento de edição específico, validação de dados, manipuladores de eventos, controle de fluxo de dados e outra lógica de negócios personalizada. A lógica de negócios do InfoPath pode ser escrita nas linguagens de programação .NET Visual Basic e C#, que são compiladas e incluídas como arquivos binários.  <br/> |
|Binária  <br/> |.dll, .exe  <br/> | Todos os componentes personalizados que fornecem lógica comercial adicional.  <br/> |
|Modelo de formulário  <br/> |.xsn  <br/> |O formato de arquivo compactado (.cab) que compacta todos os arquivos de formulário em um arquivo.  <br/> |
   

