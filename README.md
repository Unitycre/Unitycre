using System.Collections;
using System.Collections.Generic;
using System.Security.Cryptography.X509Certificates;
using UnityEngine;

public class Player : MonoBehaviour
{
    public static int score = 0;
    public static List<Square> squares;

    // Start is called before the first frame update
    void Awake()
    {
        squares = new List<Square> ();
    }

    // Update is called once per frame
    void Update()
    {
        if (squares.Count == 0)
        {
            Victory();
        }
    }
    public static void Defeat ()
    {
        score = 0;
        UI.ShowDefeatPanel();
    }

    public static void Victory()
    {
        UI.ShowVictoryPanel();
    }

    public static void Restsart()
    {
            int index = SceneManagement.GetActiveScene().buildIndex;
            SceneManager.LoadScene(index);
    }

        
   
}
