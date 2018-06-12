---
title: Bloco de dados Pesquisarregistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Um bloco de dados Pesquisarregistro executa um conjunto de ações em um registro específico.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765106"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>Bloco de dados Pesquisarregistro (aplicativo da web personalizado do Access)

Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

A ação **PesquisarRegistro** tem os seguintes argumentos. 
  
|**Argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| _Em_ <br/> |Sim  <br/> |Uma cadeia de caracteres que identifica o registro para operar em. O argumento *em* pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.  <br/> |
| _Condição onde_ <br/> |Não  <br/> |Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **Pesquisarregistro** é executada. Por exemplo, critérios costuma ser equivalente à cláusula WHERE em uma expressão SQL, sem a palavra onde. Se os critérios for omitido, o bloco de dados **Pesquisarregistro** opera em todo o domínio especificado pelo argumento *em* . Qualquer campo que está incluído nos critérios também deve ser um campo no *In* .  <br/> |
| _Alias_ <br/> |Não  <br/> |Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento *em* . Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas. Se o *Alias* não for especificado, o nome da tabela ou consulta será usado como o alias.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o critério especificado pelos argumentos  *Em*  e  *Condição Where*  especificar mais de um registro, o bloco de dados **PesquisarRegistro** será executado somente no primeiro registro. 
  
Se nenhum registro satisfizer *Condição Where* ou *se não tiver registros* , **Pesquisarregistro** cria um registro em branco no qual todos os campos contêm um valor **Nulo** . 
  

