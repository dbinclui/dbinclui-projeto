# DICAS DE ACESSIBILIDADE NO CÓDIGO

* Cuidar com o uso excessivo de **DIV** e **SPAN**. Os leitores de tela possuem um pouco de dificuldade de identificá-los (principalmente quando não há tags semânticas);

* No lugar, utilizar elementos do tipo NAV, ARTICLE, SECTION e etc;

* Importante utilizar **LABEL** nos inputs. **Não utilizar** PLACEHOLDER, pois o leitor de tela não identifica;

* Adicionar **ALT** nas imagens. Ele deve vir com uma descrição informativa sobre o que está na imagem;

* Se for uma imagem que não precisa aparecer no leitor de tela, utilizar o **alt vazio**, assim, o leitor ignora essa parte. *Ex: alt=””*;

* Usar as tags de título corretamente **H1, H2, H3, H4, H5, H6**. Recomendado ter apenas um H1 por página, pois para o leitor de tela existe apenas um título principal;

* Quando utilizar a tag **a**, os links deverão ser explicativos para o usuário saber para onde está sendo encaminhado. *Ex: Escrever “Download MongoDB” ao invés de “Download” ou “clique aqui”*;

[Referência Artigo: Pequenas Atitudes no Desenvolvimento Frontend para Grandes Benefícios na Acessibilidade](https://medium.com/totvsdevelopers/pequenas-atitudes-no-desenvolvimento-front-end-para-grandes-benef%C3%ADcios-na-acessibilidade-88f1f5b1086e)

---

* Se for possível, **evite** os traços. *Ex: Escrever 5 a 7 invés de 5 - 7*;

* Expanda as abreviações. *Ex: Dra. (melhor escrever “Doutora”)*;

* Expanda acrônimos pelo menos uma vez. Se pela primeira vez a palavra HTML surgir, escreva *Hypertext Markup Language, o HTML*;

* É possível especificar uma linha ou uma coluna em tabelas usando o atributo **SCOPE**. Exemplo: 
```
<th scope=”col”>Band</th>
```
```
<th scope=”row”> Kiss </th>
```

* O **CAPTION** serve como um texto alternativo à tabela para os usuários de leitores de tela terem acesso rápido sobre o que é o conteúdo. *Ex:*

```
<table>
	<caption> Uma tabela sobre frutas</caption>
	<thead>...</thead>
</table>
```

* **Não incluir texto dentro da imagem**. Utilizar o atributo **TITLE** para fornecer a informação;

[Referência Artigo: HTML: Boas Práticas em Acessibilidade - MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Learn/Accessibility/HTML)

---

* Sublinhado de links é útil para quem tem dificuldade de discernimento de contraste;

* Não apresentar parágrafos excessivamente longos;

* Cuidado com rolagem infinita. Pode ser problemático para quem faz a navegação por teclado;

* Cuidado com animações infinitas. Mesmo que sutis podem ser consideradas distrações para pessoas com TDAH;

* Testar se a navegação no teclado funciona;

* Incluir um **SKIP-TO-CONTENT** no topo da página. Ajuda os usuários de leitores de tela a não terem que passar por todo o cabeçalho;

* Certificar-se que os efeitos **HOVER** não limitam o acesso ao conteúdo. Tem usuários que não utilizam mouse;

* Radio buttons devem ser agrupados de preferência dentro de um fieldset com uma legenda servindo como rótulo;

* É importante utilizar o HTML semântico o quanto for possível. Caso não houver tags que contemplem certos elementos, utilize os atributos ARIA;

* Não reproduzir vídeos automaticamente. E se reproduzir, deixar sem som (podem ser irritantes ou danosos);

* Optar por alto contraste de cores;

* Não transmitir informações somente através de cores;

* Fontes light e finas tendem a ser muito difíceis de ler. Podem ser usadas em textos em que a fonte seja maior;

* Evitar interações que dependem do tempo. Cada pessoa tem seu ritmo;

* Evitar mensagens de erro que façam o usuário se sentir constrangido;

[Referência Artigo: 49 Dicas de Acessibilidade WEB](https://www.pedrodias.net/ux/dicas-de-acessibilidade-web)

---

* Evitar ao máximo alinhamento justificado, centralizado e à direita. O alinhamento à esquerda traz um ponto de referência único para o início dos textos;

* Não esquecer de informar a **linguagem do conteúdo das páginas no atributo LANG**. Os leitores de tela usam essa informação para calibrar a pronúncia;

* Usar listas;

* É possível marcar um trecho do código como sendo de uma linguagem diferente, permitindo que o leitor de telas leia com a pronúncia adequada. *Ex:* 

```
<span lang=”en”></span>
```

[Referência Artigo: Páginas Acessíveis](http://talitapagani.com/paginas-acessiveis/exemplos/navegacao/)

---

* No caso do uso das DIVs, é importante utilizar as tags semânticas do HTML para informar qual o papel dessa div no leitor de tela. *Exemplo:*

```
 <div role=”navigation”></div>

 ```

* Se a DIV está no código para agrupar elementos, substitua por 

```
<>

</>

```

* Na ordem da página, se houver título e imagem, o título vem primeiro;

[Referência Artigo: Como Criar um Site Acessível Usando React](https://www.youtube.com/watch?v=nHnocutlphc&ab_channel=Labenu)

---

* É possível tornar elementos não focaveis em focaveis, assim, facilita o acesso através do teclado. *Exemplo:*

```
<h2 tabIndex={0}> Um cabeçalho focável</h2>

```

* Nesse caso, o usuário que utiliza o teclado para navegação conseguirá realizar a leitura dos elementos que receberam esse atributo;

[Referência Artigo: Escrevendo Javascript com Acessibilidade em Mente](https://maujor.com/tutorial/escrevendo-javascript-com-acessibilidade-em-mente.php)

---

* Verifique se os blocos de formulário estão envolvidos por elementos **FIELDSET** e identificados com o elemento **LEGEND**;

* Verificar se conteúdo interativo tem foco marcado (**evite tirar o outline dos elementos** interativos quando receberem foco);

* Contraste de pelo menos 4.5:1 (segundo diretrizes da W3C);

* Verifique se a ampliação de 200% em sua página permite que o usuário consiga ler o conteúdo sem que o design seja comprometido;

[Referência Artigo: Dicas para Verificar a Acessibilidade da sua Página WEB](https://mwpt.com.br/dicas-para-verificar-acessibilidade-da-sua-pagina-web/)

---

* É importante que as páginas possuam título;

* Quando as páginas possuem título, os usuários se orientam mais facilmente pois podem identificar a localização atual sem que precisem ler a página e seu conteúdo;

* Para colocar título em páginas utilizando o React, temos que **instalar o pacote react-document-title**;

* Pessoas com deficiências visuais poderão diferenciar mais facilmente o conteúdo quando diversas páginas Web estiverem abertas, e aqueles que utilizam recursos de áudio quando estão navegando entre páginas Web também são beneficiados;

[Pacote react-document-title](https://www.npmjs.com/package/react-document-title)  

[Referência Artigo: Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-title.html)

---

# Atributos ARIA

* Diferente da maioria dos atributos e propriedades DOM no React, os atributos ARIA devem ser hypen-case ao invés de camelCase; 

* Existem 3 tipos principais de componentes: roles, states, e properties:
    - **Roles**: permite definir o papel que o elemento faz na página  e, uma vez definido, isso não muda. *Exemplo: role=”search”*;
    - **States**: representam o estado do elemento e, dessa forma, pode ter o valor alterado. *Exemplo: aria-checked*;
    - **Properties**: raramente tem o valor alterado. *Exemplo: aria-labelledby*;

* *Exemplo de uma barra de progresso utilizando ARIA:*

```
<div class="progressbar" 
	role="progressbar" 
	aria-valuemin="0" 
	aria-valuemax="100%" 
	aria-valuenow="50%" 
/>
```
[Referência Artigo: What the Heck is ARIA? A Begginer's Guide to ARIA for Acessibility](https://www.lullabot.com/articles/what-heck-aria-beginners-guide-aria-accessibility)  

[Referência Artigo: Regras de Acessibilidade para WAI-ARIA](https://ux.sapo.pt/acessibilidade/web-acessibilidade/aria/)  

[Referência Artigo: Interface ARIA Attributes](https://use-form.netlify.app/interfaces/_node_modules__types_react_index_d_.react.ariaattributes.html)











  
