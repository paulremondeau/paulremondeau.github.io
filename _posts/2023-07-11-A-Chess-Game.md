---
title: A chess game
date: 2023-07-11 17:06:00 +0200
categories: [Project]
tags: [scala, react, typescript, docker, cloud, google cloud]     # TAG names should always be lowercase
author: paul_remondeau
image:
  path: /commons/chess/chess_board_react_preview.png
  alt: A chess game in React.
katex: true
---

This project is a self-made chess game built with :

<div style="display: flex; justify-content: space-evenly">
  <div style="display: inline; align-items: center; text-align: center; padding:10px;">
    <p>Backend</p>
    <div style="display: grid;">
        <img src="/commons/stacks/scala.png" width="80" /> 
         <img src="/commons/stacks/scala_http4s.svg" width="80" /> 
    </div>

  
  </div>
  <div style="display: inline; align-items: center; text-align: center; padding:10px;">
    <p>Frontend</p>
    <div style="display: grid;">
        <img src="/commons/stacks/React.png" width="80" /> 
        <img src="/commons/stacks/typescript.png" width="80" /> 
    </div>
  </div>
   <div style="display: inline; align-items: center; text-align: center; padding:10px;">
    <p>Deployment</p>
    <div style="display: grid;">
        <img src="/commons/stacks/docker.png" width="80" /> 
        <img src="/commons/stacks/googlecloud.png" width="80" /> 
    </div>
  </div>
   <div style="display: inline; align-items: center; text-align: center;padding:10px;">
    <p>Versioning</p>
    <img src="/commons/stacks/github.png" width="80" /> 
  </div>
</div>

The goal of the project is to make a workable chess game that you can play on your computer.

Project situation :
- [x] Scala backend
- [x] Scala API
- [x] React frontend
- [x] Deployed on Google Cloud

You can find the project source code on [GitHub](https://github.com/paulremondeau/chess).

You can play with the application on this [link](https://chess-frontend-27lngjqnaq-od.a.run.app/).

## Why this project

Early 2023 I attempted to learn how to play chess. Since then I practice regularly and I found 
my interest for the game growing day after day. I play solely on [Lichess](https://lichess.org), which is an open
source chess application that allow you to play, analyse, study and pratice chess entirely for free.

On the other hand, I always like to learn new skills and tools to enhance my software engineering skills.
I stood upon the Scala language which appeals a lot to me for its Object Oriented/Functional Programming hybrid paradigm.
I therefore decided to create my own chess game application with this technology.

I plan to make a React-based Frontend in the near future to allows easy use of the application.

## Chess rules

The game of chess is played by two players (white and black) on a 8x8 board. Each player has 8 pawns,
2 rooks, 2 bishops, 2 knights, 1 queen and 1 king. The goal is to checkmate the opponents's king,
which means the opponent king is threatened with capture and has no espace.

For reminder, pieces move like this :

<div style="display: inline">

  <div style="display: flex; align-items:center; text-align: center">
    <div style="display: inline; align-items: center; text-align: center">
        <img src="/commons/chess/Pawn.gif" width="250" /> 
        <figcaption>Pawn movements</figcaption>
    </div>
    <div style="display: inline; align-items: center; text-align: center">
        <img src="/commons/chess/Rook.gif" width="250" /> 
        <figcaption>Rook movements</figcaption>
    </div>
    <div style="display: inline; align-items: center; text-align: center">
        <img src="/commons/chess/Bishop.gif" width="250" /> 
        <figcaption>Bishop movements</figcaption>
    </div>
  </div>

  <div style="display: flex; align-items:center; text-align: center">
    <div style="display: inline; align-items: center; text-align: center">
        <img src="/commons/chess/Knight.gif" width="250" /> 
        <figcaption>Knight movements</figcaption>
    </div>
    <div style="display: inline; align-items: center; text-align: center">
        <img src="/commons/chess/Queen.gif" width="250" /> 
        <figcaption>Queen movements</figcaption>
    </div>
    <div style="display: inline; align-items: center; text-align: center">
        <img src="/commons/chess/King.gif" width="250" /> 
        <figcaption>King movements</figcaption>
    </div>
  </div>

</div>


## Scala backend

The backend of the application is made in Scala. You can find the documentation of the backend at this [link](https://paulremondeau.github.io/chess/).

A game of chess can be created using the [Game](https://paulremondeau.github.io/chess/_empty_/Game.html) class.
A game contains a [Board](https://paulremondeau.github.io/chess/_empty_/Board.html) which contains all the [Pieces](https://paulremondeau.github.io/chess/_empty_/Piece.html).

The game goes on like this :
* The player choose its piece to move.
* The player choose the square it wants to move the piece on.
* It's the opponent turn.
* It goes on until one of them wins, or a draw appears.

To debug the main game, it was usefull to print the board in the terminal :
![BDD](/commons/chess/chess_board_scala.png)
*The chess board in the terminal*


## React Frontend

The frontend of the application is made in React and TypeScript. 

![BDD](/commons/chess/chess_board_react.png)
*The chess board of the React application. Here white has its king in check and must defend it. It can for example move the selected knight on e4 on the only two valid squares d2 and c4*

## Deployment

Both the backend and the frontend are built with docker and deployed to Google cloud. 
