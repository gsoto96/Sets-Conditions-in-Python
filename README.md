# Sets-Conditions-in-Python
{
  "metadata": {
    "language_info": {
      "codemirror_mode": {
        "name": "python",
        "version": 3
      },
      "file_extension": ".py",
      "mimetype": "text/x-python",
      "name": "python",
      "nbconvert_exporter": "python",
      "pygments_lexer": "ipython3",
      "version": "3.8"
    },
    "kernelspec": {
      "name": "python",
      "display_name": "Pyolite",
      "language": "python"
    }
  },
  "nbformat_minor": 4,
  "nbformat": 4,
  "cells": [
    {
      "cell_type": "markdown",
      "source": "Sets & Conditions in Python\nEstimated time needed: 40 minutes\n\nObjectives\nAfter completing this lab you will be able to:\n\nWork with sets in Python, including operations and logic operations.\nWork with condition statements in Python, including operators, and branching.",
      "metadata": {}
    },
    {
      "cell_type": "code",
      "source": "# Create a set\n\nset1 = {\"pop\", \"rock\", \"soul\", \"hard rock\", \"rock\", \"R&B\", \"rock\", \"disco\"}\nset1",
      "metadata": {
        "trusted": true
      },
      "execution_count": 326,
      "outputs": [
        {
          "execution_count": 326,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'R&B', 'disco', 'hard rock', 'pop', 'rock', 'soul'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Convert list to set\n\nalbum_list = [ \"Michael Jackson\", \"Thriller\", 1982, \"00:42:19\", \\\n              \"Pop, Rock, R&B\", 46.0, 65, \"30-Nov-82\", None, 10.0]\nalbum_set = set(album_list)             \nalbum_set",
      "metadata": {
        "trusted": true
      },
      "execution_count": 327,
      "outputs": [
        {
          "execution_count": 327,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'00:42:19',\n 10.0,\n 1982,\n '30-Nov-82',\n 46.0,\n 65,\n 'Michael Jackson',\n None,\n 'Pop, Rock, R&B',\n 'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Convert list to set\n\nmusic_genres = set([\"pop\", \"pop\", \"rock\", \"folk rock\", \"hard rock\", \"soul\", \\\n                    \"progressive rock\", \"soft rock\", \"R&B\", \"disco\"])\nmusic_genres",
      "metadata": {
        "trusted": true
      },
      "execution_count": 328,
      "outputs": [
        {
          "execution_count": 328,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'R&B',\n 'disco',\n 'folk rock',\n 'hard rock',\n 'pop',\n 'progressive rock',\n 'rock',\n 'soft rock',\n 'soul'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Sample set\n\nA = set([\"Thriller\", \"Back in Black\", \"AC/DC\"])\nA",
      "metadata": {
        "trusted": true
      },
      "execution_count": 329,
      "outputs": [
        {
          "execution_count": 329,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black', 'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Add element to set\n\nA.add(\"NSYNC\")\nA",
      "metadata": {
        "trusted": true
      },
      "execution_count": 330,
      "outputs": [
        {
          "execution_count": 330,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black', 'NSYNC', 'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Try to add duplicate element to the set\n\nA.add(\"NSYNC\")\nA",
      "metadata": {
        "trusted": true
      },
      "execution_count": 331,
      "outputs": [
        {
          "execution_count": 331,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black', 'NSYNC', 'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Remove the element from set\n\nA.remove(\"NSYNC\")\nA",
      "metadata": {
        "trusted": true
      },
      "execution_count": 332,
      "outputs": [
        {
          "execution_count": 332,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black', 'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Verify if the element is in the set\n\n\"AC/DC\" in A",
      "metadata": {
        "trusted": true
      },
      "execution_count": 333,
      "outputs": [
        {
          "execution_count": 333,
          "output_type": "execute_result",
          "data": {
            "text/plain": "True"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Sample Sets\n\nalbum_set1 = set([\"Thriller\", 'AC/DC', 'Back in Black'])\nalbum_set2 = set([ \"AC/DC\", \"Back in Black\", \"The Dark Side of the Moon\"])",
      "metadata": {
        "trusted": true
      },
      "execution_count": 334,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Print two sets\n\nalbum_set1, album_set2",
      "metadata": {
        "trusted": true
      },
      "execution_count": 335,
      "outputs": [
        {
          "execution_count": 335,
          "output_type": "execute_result",
          "data": {
            "text/plain": "({'AC/DC', 'Back in Black', 'Thriller'},\n {'AC/DC', 'Back in Black', 'The Dark Side of the Moon'})"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Find the intersections\n\nintersection = album_set1 & album_set2\nintersection",
      "metadata": {
        "trusted": true
      },
      "execution_count": 336,
      "outputs": [
        {
          "execution_count": 336,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Find the difference in set1 but not set2\n\nalbum_set1.difference(album_set2)  ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 337,
      "outputs": [
        {
          "execution_count": 337,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "album_set2.difference(album_set1)  ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 338,
      "outputs": [
        {
          "execution_count": 338,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'The Dark Side of the Moon'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Use intersection method to find the intersection of album_list1 and album_list2\n\nalbum_set1.intersection(album_set2)   ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 339,
      "outputs": [
        {
          "execution_count": 339,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Find the union of two sets\n\nalbum_set1.union(album_set2)",
      "metadata": {
        "trusted": true
      },
      "execution_count": 340,
      "outputs": [
        {
          "execution_count": 340,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black', 'The Dark Side of the Moon', 'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Check if superset\n\nset(album_set1).issuperset(album_set2)   ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 347,
      "outputs": [
        {
          "execution_count": 347,
          "output_type": "execute_result",
          "data": {
            "text/plain": "False"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Check if subset\n\nset(album_set2).issubset(album_set1)     ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 348,
      "outputs": [
        {
          "execution_count": 348,
          "output_type": "execute_result",
          "data": {
            "text/plain": "False"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Check if subset\n\nset({\"Back in Black\", \"AC/DC\"}).issubset(album_set1) ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 349,
      "outputs": [
        {
          "execution_count": 349,
          "output_type": "execute_result",
          "data": {
            "text/plain": "True"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Check if superset\n\nalbum_set1.issuperset({\"Back in Black\", \"AC/DC\"})   ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 350,
      "outputs": [
        {
          "execution_count": 350,
          "output_type": "execute_result",
          "data": {
            "text/plain": "True"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Convert the list ['rap','house','electronic music', 'rap'] to a set:\nmusic_genres = set(['rap','house','electronic music', 'rap', \\\n                    'rap','house','electronic music', 'rap'])\nmusic_genres",
      "metadata": {
        "trusted": true
      },
      "execution_count": 377,
      "outputs": [
        {
          "execution_count": 377,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'electronic music', 'house', 'rap'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Consider the list A = [1, 2, 2, 1] and set B = set([1, 2, 2, 1]), does sum(A) == sum(B)?\nA = [1, 2, 2, 1]  \nB = set([1, 2, 2, 1])\nprint(\"the sum of A is:\", sum(A))\nprint(\"the sum of B is:\", sum(B))",
      "metadata": {
        "trusted": true
      },
      "execution_count": 378,
      "outputs": [
        {
          "name": "stdout",
          "text": "the sum of A is: 6\nthe sum of B is: 3\n",
          "output_type": "stream"
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "#Create a new set <code>album_set3</code> that is the union of <code>album_set1</code> and <code>album_set2</code>:\n    # Write your code below and press Shift+Enter to execute\n\nalbum_set1 = set([\"Thriller\", 'AC/DC', 'Back in Black'])\nalbum_set2 = set([ \"AC/DC\", \"Back in Black\", \"The Dark Side of the Moon\"])\nalbum_set3 = album_set1.union(album_set2)\nalbum_set3\n",
      "metadata": {
        "trusted": true
      },
      "execution_count": 379,
      "outputs": [
        {
          "execution_count": 379,
          "output_type": "execute_result",
          "data": {
            "text/plain": "{'AC/DC', 'Back in Black', 'The Dark Side of the Moon', 'Thriller'}"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Find out if album_set1 is a subset of album_set3:\nalbum_set1.issubset(album_set3)",
      "metadata": {
        "trusted": true
      },
      "execution_count": 380,
      "outputs": [
        {
          "execution_count": 380,
          "output_type": "execute_result",
          "data": {
            "text/plain": "True"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": "\nCondition Statements",
      "metadata": {}
    },
    {
      "cell_type": "code",
      "source": "# Condition Equal\n\na = 5\na == 6",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Greater than Sign\n\ni = 6\ni > 5",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Greater than Sign\n\ni = 2\ni > 5",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Inequality Sign\n\ni = 2\ni != 6",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Inequality Sign\n\ni = 6\ni != 6",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Use Equality sign to compare the strings\n\n\"ACDC\" == \"Michael Jackson\"",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Use Inequality sign to compare the strings\n\n\"ACDC\" != \"Michael Jackson\"",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Compare characters\n\n'B' > 'A'",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Compare characters\n\n'BA' > 'AB'",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# If statement example\n\nage = 19\n#age = 18\n\n#expression that can be true or false\nif age > 18:\n    \n    #within an indent, we have the expression that is run if the condition is true\n    print(\"you can enter\" )\n\n#The statements after the if statement will run regardless if the condition is true or false \nprint(\"move on\")",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Else statement example\n\nage = 18\n# age = 19\n\nif age > 18:\n    print(\"you can enter\" )\nelse:\n    print(\"go see Meat Loaf\" )\n    \nprint(\"move on\")",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Elif statment example\n\nage = 18\n\nif age > 18:\n    print(\"you can enter\" )\nelif age == 18:\n    print(\"go see Pink Floyd\")\nelse:\n    print(\"go see Meat Loaf\" )\n    \nprint(\"move on\")",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Condition statement example\n\nalbum_year = 1983\nalbum_year = 1970\n\nif album_year > 1980:\n    print(\"Album year is greater than 1980\")\n    \nprint('do something..')",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Condition statement example\n\nalbum_year = 1983\n#album_year = 1970\n\nif album_year > 1980:\n    print(\"Album year is greater than 1980\")\nelse:\n    print(\"less than 1980\")\n\nprint('do something..')",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Condition statement example\n\nalbum_year = 1980\n\nif(album_year > 1979) and (album_year < 1990):\n    print (\"Album year was in between 1980 and 1989\")\n    \nprint(\"\")\nprint(\"Do Stuff..\")",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Condition statement example\n\nalbum_year = 1990\n\nif(album_year < 1980) or (album_year > 1989):\n    print (\"Album was not made in the 1980's\")\nelse:\n    print(\"The Album was made in the 1980's \")",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "# Condition statement example\n\nalbum_year = 1983\n\nif not (album_year == 1984):\n    print (\"Album year is not 1984\")",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": "#  Write an if statement to determine if an album had a rating greater than 8. Test it using the rating for the album “Back in Black” that had a rating of 8.5. If the statement is true print \"This album is Amazing!\"\nalbum_rating = 8.5\n\nif(album_rating > 8):\n    print (\"This album is Amazing!\")",
      "metadata": {
        "trusted": true
      },
      "execution_count": 382,
      "outputs": [
        {
          "name": "stdout",
          "text": "This album is Amazing!\n",
          "output_type": "stream"
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Write an if-else statement that performs the following. If the rating is larger then eight print “this album is amazing”. If the rating is less than or equal to 8 print “this album is ok”.\n\nrating = 6\n\nif rating > 8:\n    print (\"this album is amazing\")\nelse:\n    print (\"this album is ok\")\n",
      "metadata": {
        "trusted": true
      },
      "execution_count": 391,
      "outputs": [
        {
          "name": "stdout",
          "text": "this album is ok\n",
          "output_type": "stream"
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "# Write an if statement to determine if an album came out before 1980 or in the years: 1991 or 1993. If the condition is true print out the year the album came out.\nrelease = 1979\nif release < 1980 or release == 1991 or release == 1993:\n    print(\"This album came out in year\", release)\n    ",
      "metadata": {
        "trusted": true
      },
      "execution_count": 394,
      "outputs": [
        {
          "name": "stdout",
          "text": "This album came out in year 1979\n",
          "output_type": "stream"
        }
      ]
    },
    {
      "cell_type": "code",
      "source": "",
      "metadata": {},
      "execution_count": null,
      "outputs": []
    }
  ]
}
