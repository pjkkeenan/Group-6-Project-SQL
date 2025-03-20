# Group-6-Project-SQL
# MIST4610-Project-1
MIST 4610 - Project 1 
<h1>TEAM MEMBERS (21484_G6)</h1>
<li>Ademoye, Adekanle <a href="url">link for github</a></li>
<li>Keenan, Patrick <a href="https://github.com/pjkkeenan">link for github</a></li>
<li>Patel, Kishan <a href="url">link for github</a></li>
<li>Thomas, Reuben <a href="https://github.com/Reubenuga">rmt08737</a></li>
<li>Patel, Nidhi <a href="https://github.com/ndp88405">ndp88405</a></li>

<h1>Problem Description</h1>
<p>The state of Georgia is home to many great sports teams, including the Braves, Hawks, Bulldogs, and Falcons. The latter two, in particular, command attention from TV screens across the Peach State. From tears and sweat to excitement and joy, football means everything to the state. To meet the growing demand for football, we come to the GFL, a new chapter in Georgia’s rich football legacy. The GFL aims to elevate the state’s passion for the sport while setting the stage for other states to adopt this fresh take on America’s favorite game.
However, launching the league comes with challenges, especially in managing and organizing its operations. From overseeing the inaugural 10 teams and their players and staff to scheduling games and handling financial contracts, the GFL needs a robust system to ensure smooth operations. The solution lies in a centralized database that streamlines data management, enabling real-time information access. This enhances reporting capabilities and decision-making, laying a solid foundation for the GFL to grow into a major league, one capable of delivering entertainment on par with the NFL. </p>

<h1>Data Model</h1>
<p>Our data model is based on a hypothetical Football League based in Georgia. It captures key aspects of team organization, player management, staff roles, sponsorships, and league affiliations. 

At its core, the <b> Player</b> table holds detailed information about the individual athletes, like their physical attributes, position, and team affiliation. Each player is linked to a specific <b>Position</b>, which defines their roles on the field. The positions include quarterback, wide receiver, offensive lineman, defensive lineman, safety, and cornerback. The players’ contract details are stored in the <b>Contracts</b> table, which tracks their salary, start and end dates of the contract. 

Players belong to a <b>Team </b>, which is identified by the name, city and their associate home venue, which is stored in the <b>Venue</b> table, which also records the stadium capacity. Since there are 10 teams in the league we needed to make sure we had additional organizational elements which included, sponsorship agreements captured in the <b>Sponsor</b> table, which details sponsoring companies and the type of sponsor the company is, like Beverage, Airlines, or Transportation. 

The <b> Coach </b> table links specific coaches to teams, while the <b> Staff </b> table holds information on other essential personnel, such as medical staff. The <b>team_Staff</b> table facilitates a many-to-many relationship between teams and their staff members. Teams also have designated uniforms, recorded in the <b>Uniform</b> table, which captures uniform colors, patterns, and materials. 

Beyond individual teams, the model accounts for league structures through the <b>Conference</b> table, which categorizes teams based on geographical location, East or West. The <b>teamConference</b> table establishes a many-to-many relationship between teams and conferences, enabling teams to participate in multiple league structures. 

</p>
<img alt="Data Model" src="https://github.com/user-attachments/assets/1758a320-708e-4a1e-868f-c8baf724b529"/>



<h1>Data Dictionary</h1>
<img width="630" alt="Player" src="https://github.com/user-attachments/assets/cd33ce3d-1ffd-4493-85dd-b79ddc3c1d6c" />
<img width="630" alt="team_Staff" src="https://github.com/user-attachments/assets/75bb0d68-c446-4044-bc38-0e8515f84738" />
<img width="629" alt="Staff" src="https://github.com/user-attachments/assets/e075acbe-8154-4e6a-9a53-c8514f21e7b3" />
<img width="629" alt="Uniform" src="https://github.com/user-attachments/assets/a6257ac0-3062-46e5-bbb3-34be07f26a2f" />
<img width="629" alt="Positions" src="https://github.com/user-attachments/assets/3a027fd8-c28c-462e-970f-91c6309c5a39" />
<img width="629" alt="Venue" src="https://github.com/user-attachments/assets/36b0de15-75a9-47d5-86a3-fbf22a6a8ab9" />
<img width="629" alt="Sponsor" src="https://github.com/user-attachments/assets/d941eaf7-2e33-49ef-8568-c589bc5c848c" />
<img width="629" alt="Contracts" src="https://github.com/user-attachments/assets/4770d067-086f-4b5c-b168-6143585f7f8c" />
<img width="629" alt="team_Conference" src="https://github.com/user-attachments/assets/6539e820-d47b-4033-84d0-57466212b07a" />
<img width="629" alt="Conference" src="https://github.com/user-attachments/assets/f066e66a-d912-4738-8f99-da102ce8b6b9" />

<h1>Queries</h1>
<img src="https://github.com/user-attachments/assets/24747a6c-bc04-445a-ad56-144c75e9211d"/>
<h3>Query 1</h3>
<p>List players full name that play in the quarterback position</p>
<img width="629"src="https://github.com/user-attachments/assets/4a52c5db-9e9f-41f2-9254-0045b34af652"/>
<p>A manager would be interested in this query result to identify all players who play in the quarterback position. This allows them to evaluate the talent pool in that specific role, compare quarterbacks across teams, and assess their team's needs in terms of recruiting or contract negotiations. By focusing on a key position, such as quarterback, managers can make informed decisions about player development, team strategy, and matchups with other teams. It also helps with team roster management by clearly outlining which players fulfill critical roles.</p>

<h3>Query 2</h3>
<p>List the player id, full name weight and team name of players that weight more than the average weight for there team </p>
<img width="629" src="https://github.com/user-attachments/assets/5b573fc5-6cee-43c1-bd03-b00adb96dc6c"/>
<p>A manager would be interested in this query result to identify players who weigh more than the average for their team. This information helps the manager track physical attributes and assess if any players might benefit from adjustments in their diet or training regimen. Monitoring these players is important for ensuring they maintain optimal health and performance levels. Additionally, this can help the manager identify players who may have a physical advantage over their teammates, potentially influencing their role on the team or how their physical attributes are utilized during games.</p>

<h3>Query 3</h3>
<p>The full player name, salary, team, conference where they earn a salary more than 800,000 and play in the eastern conference</p>
<img width="629" src ="https://github.com/user-attachments/assets/4418a27b-9a48-4859-aea8-f84b565248a2"/>
<p>A manager would be interested in this query result to gain insights into high-earning players in the Eastern Conference. This information can help with budget planning, determining salary cap allocations, and understanding player value within the conference. By identifying players who earn more than a specific threshold, managers can assess whether their team's salary distribution aligns with the league’s financial landscape. It also enables the manager to make informed decisions when negotiating contracts or analyzing competitive trends in the conference.</p>

<h3>Query 4</h3>
<p>Find the tallest and heaviest players and their full name weight and team name</p>
<img width="629" src ="https://github.com/user-attachments/assets/5f4fcf98-22b7-4730-8437-4534adc0af6f"/>
<p>A manager would be interested in this query result to compare their team's tallest and heaviest players against others. This information can be useful for assessing physical attributes that may provide competitive advantages in certain positions. Understanding how their biggest players stack up can help with training strategies, recruitment decisions, and game planning. Additionally, it allows managers to evaluate whether their team's roster meets the physical demands of the league and make adjustments if necessary.</p>

<h3>Query 5</h3>
<p>The average payroll of each Team and order it from high to low</p>
<img width="629" src ="https://github.com/user-attachments/assets/03056969-21ad-402a-8394-7e4562afa11f">
<p>A manager would be interested in this query result to track the average payroll of each team and compare spending across the league. This helps in understanding financial competitiveness, identifying teams with higher budgets, and evaluating how salary distribution correlates with team performance. By analyzing payroll trends, managers can make strategic decisions regarding player contracts, budgeting, and resource allocation. Additionally, it provides insights into market trends, helping teams stay competitive while maintaining financial sustainability.</p>

<h3>Query 6</h3>
<p>All the players who share the last name Lambert along with there playerID age team name </p>
<img width="629" src = "https://github.com/user-attachments/assets/1b6f39fe-ca06-4c5e-a23d-3a23493e6c9b"/>
<p>A manager would be interested in this query result to identify players with the last name "Lambert," as they could be related. This information can help in team dynamics, marketing, or even contract negotiations if family connections influence player decisions. Identifying related players could also provide insights into chemistry on the field, as relatives may have a natural rapport. Additionally, it allows for personalized engagement strategies, such as promoting family connections within the team for fan engagement or media opportunities.</p>

<h3>Query 7</h3>
<p> The highest paid player and the team they play for along with there age playedID and show there Salary </p>
<img width="629" src ="https://github.com/user-attachments/assets/2aff59d5-82d1-4366-bc87-d61302912534"/>
<p>A manager would be interested in this query result to see which player has the highest salary and compare it to their own team's salary structure. This information is useful for evaluating payroll distribution, ensuring fair compensation, and making informed decisions about contract negotiations. Understanding how their team's salaries compare to the highest-paid player can help in budgeting, assessing player value, and maintaining competitive financial planning. Additionally, it provides insights into market trends and potential adjustments needed for future salary negotiations.</p>

<h3>Query 8</h3>
<p>Players whose contracts expire within the next 2 years</p>
<img width="629" src = "https://github.com/user-attachments/assets/7996ff08-bed9-425f-8b37-240a06be6668"/>
<p>A manager would be interested in this query result to track players whose contracts are set to expire within the next two years. This allows them to proactively negotiate contract extensions, plan for potential replacements, and ensure key players remain with the team. By identifying expiring contracts in advance, managers can avoid last-minute negotiations, budget accordingly for future signings, and maintain team stability. Additionally, it helps in strategic roster planning, ensuring the team remains competitive without unexpected player departures.</p>

<h3>Query 9</h3>
<p>Coaches name and date of birth that were born before 1980</p>
<img src="https://github.com/user-attachments/assets/76d9a231-b1a5-4071-8581-0935b930f608"/>
<p>A manager would be interested in this query result to identify coaches born before 1980 who may be approaching retirement. This information is valuable for succession planning, ensuring smooth leadership transitions, and preparing for potential staff changes. It also aids in contract management, allowing the organization to assess renewal or replacement needs. Additionally, understanding the age distribution of coaches helps in workforce strategy, ensuring continuity in team leadership. By proactively analyzing this data, managers can make informed decisions to maintain team stability and long-term success.</p>

<h3>Query 10</h3>
<p>A venue that contains the letter B and order by the capacity ascending</p>
<img src="https://github.com/user-attachments/assets/993102e2-dedf-4dad-a849-d8f5b822edb3"/>
<p>A manager would be interested in this query result to identify venues that contain the letter "B" in their name and compare their capacities. Ordering the results by ascending capacity allows managers to quickly assess smaller venues first, which could be useful for planning events, scheduling games, or evaluating potential locations for team activities. Understanding venue sizes helps in making informed decisions regarding ticket sales, audience accommodation, and logistical arrangements for events.</p>

<h1> Database Information</h1>
<p> al_Group_21484_G6</p>




