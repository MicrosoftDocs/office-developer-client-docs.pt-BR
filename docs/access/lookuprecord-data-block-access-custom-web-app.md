---
title: Bloco de dados Pesquisarregistro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Um bloco de dados PesquisarRegistro executa um conjunto de ações em um registro específico.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304267"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>Bloco de dados Pesquisarregistro (aplicativo Web personalizado do Access)

Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

A ação **PesquisarRegistro** tem os seguintes argumentos. 
  
|**Argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| _No_ <br/> |Sim  <br/> |Uma cadeia de caracteres que identifica o registro a ser utilizado. O argumento *in* pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.  <br/> |
| _Condição Where_ <br/> |Não  <br/> |Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **PesquisarRegistro** opera. Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE. Se criteria for omitido, o bloco de dados **pesquisarregistro** funcionará em todo o domínio especificado pelo argumento *in* . Qualquer campo incluído nos critérios também deve ser um campo no *no* .  <br/> |
| _Alias_ <br/> |Não  <br/> |Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento *in* . Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas. Se *alias* não for especificado, o nome da tabela ou da consulta será usado como o alias.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o critério especificado pelos argumentos  *Em*  e  *Condição Where*  especificar mais de um registro, o bloco de dados **PesquisarRegistro** será executado somente no primeiro registro. 
  
Se nenhum registro satisfizer *em que condição* ou se *in* não contiver registros, **pesquisarregistro** cria um registro em branco no qual todos os campos contêm um valor **nulo** . 
  

