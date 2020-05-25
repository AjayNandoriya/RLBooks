<html>
<body>
    <h1>
        <a href="http://incompleteideas.net/book/the-book.html">Reinforcement Learning: An Introduction</a>
        By <a href="http://incompleteideas.net/index.html">Richard S. Sutton</a>
        and <a href="https://people.cs.umass.edu/~barto/">G. Barto</a>
    </h1>
    <p>
        <h1>
            Exercises: Chapter-1
        </h1>
    </p>
    <ol>
        <li>
            <details>
                <summary><b>Self-Play Suppose, instead of playing against a random opponent, the
                        reinforcement learning algorithm described above played against itself, with both sides
                        learning. What do you think would happen in this case? Would it learn a diferent policy for
                        selecting moves?</b></summary>
                <pre>
                    Answer 1.1
                </pre>
            </details>
        </li>
        <li>
            <details>
                <summary><b>Symmetries Many tic-tac-toe positions appear di↵erent but are really
                        the same because of symmetries. How might we amend the learning process described
                        above to take advantage of this? In what ways would this change improve the learning
                        process? Now think again. Suppose the opponent did not take advantage of symmetries.
                        In that case, should we? Is it true, then, that symmetrically equivalent positions should
                        necessarily have the same value?
                    </b></summary>
                        <pre>
                        Answer 1.2
                    </pre>
            </details>
        </li>
        <li>
            <details>
                <summary><b>Greedy Play Suppose the reinforcement learning player was greedy, that is,
                        it always played the move that brought it to the position that it rated the best. Might it
                        learn to play better, or worse, than a nongreedy player? What problems might occur?
                    </b></summary>
                <pre>
                    Answer 1.3
                </pre>
            </details>
        </li>
        <li>
            <details>
                <summary><b>Learning from Exploration Suppose learning updates occurred after all
                        moves, including exploratory moves. If the step-size parameter is appropriately reduced
                        over time (but not the tendency to explore), then the state values would converge to
                        a diferent set of probabilities. What (conceptually) are the two sets of probabilities
                        computed when we do, and when we do not, learn from exploratory moves? Assuming
                        that we do continue to make exploratory moves, which set of probabilities might be better to
                        learn? Which would result in more wins?
                    </b></summary>
                <pre>
                    Answer 1.4
                </pre>
            </details>
        </li>
        <li>
            <details>
                <summary><b>Other Improvements Can you think of other ways to improve the reinforcement learning player? Can
                        you think of any better way to solve the tic-tac-toe problem as posed?
                    </b></summary>
                <pre>
                    Answer 1.5
                </pre>
            </details>
        </li>
    </ol>
</body>

</html>