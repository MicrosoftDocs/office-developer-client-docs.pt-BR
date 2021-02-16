---
title: Bloco de dados LookupRecord (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Um bloco de dados PesquisarRegistro executa um conjunto de ações em um registro específico.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434358"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>Bloco de dados LookupRecord (aplicativo Web personalizado do Access)

Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Setting

A ação **PesquisarRegistro** tem os seguintes argumentos. 
  
|**Argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| _Em_ <br/> |Sim  <br/> |Uma cadeia de caracteres que identifica o registro a ser utilizado. O  *argumento In*  pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.  <br/> |
| _Condição Where_ <br/> |Não  <br/> |Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **PesquisarRegistro** opera. Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE. Se os critérios são omitidos, o bloco de dados **LookupRecord** opera em todo o domínio especificado pelo  *argumento*  In. Qualquer campo incluído nos critérios também deve ser um campo em  *In*  .  <br/> |
| _Alias_ <br/> |Não  <br/> |Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo  *argumento*  In. Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas. Se  *Alias*  não for especificado, o nome da tabela ou consulta será usado como o alias.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o critério especificado pelos argumentos  *Em*  e  *Condição Where*  especificar mais de um registro, o bloco de dados **PesquisarRegistro** será executado somente no primeiro registro. 
  
Se nenhum registro satisfaça  *Condição*  Onde ou se  *Em*  não contiver registros, **LookupRecord** criará um registro em branco no qual todos os campos contêm um **valor** Null. 
  

